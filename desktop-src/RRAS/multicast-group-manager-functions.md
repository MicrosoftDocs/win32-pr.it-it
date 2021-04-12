---
title: Funzioni di gestione gruppi multicast
description: Le funzioni seguenti vengono utilizzate per eseguire la registrazione con il gestore del gruppo multicast
ms.assetid: d4374ced-06ea-49dd-8f52-0d06612aa4c3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bbc3dbcfe24e63283907e5e68f211fd1f4cb6e3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332124"
---
# <a name="multicast-group-manager-functions"></a>Funzioni di gestione gruppi multicast

Per eseguire la registrazione con il gestore del gruppo multicast vengono utilizzate le funzioni seguenti:

[**MgmRegisterMProtocol**](/windows/desktop/api/Mgm/nf-mgm-mgmregistermprotocol)

[**MgmDeRegisterMProtocol**](/windows/desktop/api/Mgm/nf-mgm-mgmderegistermprotocol)

Per gestire la proprietà dell'interfaccia vengono usate le funzioni seguenti:

[**MgmGetProtocolOnInterface**](/windows/desktop/api/Mgm/nf-mgm-mgmgetprotocoloninterface)

[**MgmTakeInterfaceOwnership**](/windows/desktop/api/Mgm/nf-mgm-mgmtakeinterfaceownership)

[**MgmReleaseInterfaceOwnership**](/windows/desktop/api/Mgm/nf-mgm-mgmreleaseinterfaceownership)

Per gestire l'appartenenza al gruppo vengono utilizzate le funzioni seguenti:

[**MgmAddGroupMembershipEntry**](/windows/desktop/api/Mgm/nf-mgm-mgmaddgroupmembershipentry)

[**MgmDeleteGroupMembershipEntry**](/windows/desktop/api/Mgm/nf-mgm-mgmdeletegroupmembershipentry)

Le funzioni seguenti vengono utilizzate per ottenere le statistiche di inoltring multicast (MFE) e MFE:

[**MgmGetFirstMfe**](/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfe)

[**MgmGetNextMfe**](/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfe)

[**MgmGetMfe**](/windows/desktop/api/Mgm/nf-mgm-mgmgetmfe)

[**MgmGetFirstMfeStats**](/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfestats)

[**MgmGetNextMfeStats**](/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfestats)

[**MgmGetMfeStats**](/windows/desktop/api/Mgm/nf-mgm-mgmgetmfestats)

Per modificare MFE, viene usata la funzione seguente:

[**MgmSetMfe**](/windows/desktop/api/Mgm/nf-mgm-mgmsetmfe)

Vengono usate le funzioni seguenti per ottenere un elenco di gruppi che sono stati aggiunti:

[**MgmGroupEnumerationStart**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationstart)

[**MgmGroupEnumerationGetNext**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationgetnext)

[**MgmGroupEnumerationEnd**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationend)

 

 




