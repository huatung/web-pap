# @desc makefile for Server
# @author viticm<viticm.ti@gmail.com>
# @date 2013-06-25 20:00:06
include ../../premake.mk

CFLAGS  = -I$(BASEDIR)/Server/EventModule -I$(BASEDIR)/Server/Item -I$(BASEDIR)/Server/Script -I$(BASEDIR)/Server/Main -I$(BASEDIR)/Server/Obj -I$(BASEDIR)/Server/Team -I$(BASEDIR)/Server/DB -I$(BASEDIR)/Server/MenPai -I$(BASEDIR)/Server/Packets -I$(BASEDIR)/Server/AI -I$(BASEDIR)/Server/Player -I$(BASEDIR)/Server/ActionModule -I$(BASEDIR)/Server/Skills -I$(BASEDIR)/Server/Skills/SpecialObjLogic -I$(BASEDIR)/Server/Skills/SkillLogic -I$(BASEDIR)/Server/Skills/SkillLogic/Item -I$(BASEDIR)/Server/Skills/SkillLogic/Common -I$(BASEDIR)/Server/Skills/SkillLogic/Human -I$(BASEDIR)/Server/Skills/SkillLogic/Pet -I$(BASEDIR)/Server/Skills/ImpactLogic -I$(BASEDIR)/Server/Mission -I$(BASEDIR)/Server/Ability -I$(BASEDIR)/Server/Other -I$(BASEDIR)/Server/Scene -I$(BASEDIR)/Server/Scene/Scan -I$(BASEDIR)/Server/SMU -I$(BASEDIR)/Server/Base -I$(BASEDIR)/Server
LDFLAGS =
DIRS =  SpecialObjLogic SkillLogic ImpactLogic
OBJS =  ImpactLogics.o \
		Combat_Core.o \
		Skill_Core.o \
		RelationshipChecker.o \
		TargetChecker.o \
		SkillLogics.o \
		ConditionAndDeplete_Core.o \
		TargetingAndDepletingParams.o \
		LogicManager.o \
		Impact_Core.o \
		ScriptLogic.o \
		SkillInfo.o

debug:$(OBJS)
	for dir in $(DIRS); do \
		$(MAKE) debug -C $$dir; \
	done

release:$(OBJS)
	for dir in $(DIRS); do \
		$(MAKE) release -C $$dir; \
	done

all:debug

clean:
	$(RM) -f *.o
