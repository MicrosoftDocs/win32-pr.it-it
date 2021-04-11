---
title: Interfacce QMGR
description: Utilizzare le seguenti interfacce di gestione code (QMGR) per scaricare i file e monitorare i processi nella coda di download.
ms.assetid: b5b59d4f-fa18-4225-8b6f-5d4033c61650
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51cc571dcc5bbf182b3f715ee34bb6c3e94b5502
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104220972"
---
# <a name="qmgr-interfaces"></a>Interfacce QMGR

\[Le interfacce di gestione code (QMGR) sono disponibili per l'uso nei sistemi operativi specificati nella sezione requisiti di un argomento. Possono essere modificati o non disponibili nelle versioni successive. Usare invece le [interfacce bits](bits-interfaces.md).\]

Utilizzare le seguenti interfacce di gestione code (QMGR) per scaricare i file e monitorare i processi nella coda di download.



| Interfaccia                                                                 | Descrizione                                                                                                                                                   |
|---------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IBackgroundCopyCallback1**](/windows/desktop/api/Qmgr/nn-qmgr-ibackgroundcopycallback1)<br/>   | Implementare per ricevere una notifica quando si verificano gli eventi.<br/>                                                                                               |
| [**IBackgroundCopyGroup**](/windows/desktop/api/Qmgr/nn-qmgr-ibackgroundcopygroup)<br/>           | Utilizzare per gestire il gruppo. Ad esempio, aggiungere un processo al gruppo, impostare le proprietà del gruppo e avviare e arrestare il gruppo nella coda di download.<br/> |
| [**IBackgroundCopyJob1**](/windows/desktop/api/Qmgr/nn-qmgr-ibackgroundcopyjob1)<br/>             | Usare per aggiungere file al processo e recuperare lo stato del processo.<br/>                                                                                         |
| [**IBackgroundCopyQMgr**](/windows/desktop/api/Qmgr/nn-qmgr-ibackgroundcopyqmgr)<br/>             | Utilizzare per creare un nuovo gruppo, recuperare un gruppo esistente o enumerare tutti i gruppi nella coda.<br/>                                                       |
| [**IEnumBackgroundCopyGroups**](/windows/desktop/api/Qmgr/nn-qmgr-ienumbackgroundcopygroups)<br/> | Utilizzare per recuperare un elenco di gruppi nella coda di download.<br/>                                                                                            |
| [**IEnumBackgroundCopyJobs1**](/windows/desktop/api/Qmgr/nn-qmgr-ienumbackgroundcopyjobs1)<br/>   | Utilizzare per recuperare un elenco di processi nel gruppo.<br/>                                                                                                       |



 

 

 





