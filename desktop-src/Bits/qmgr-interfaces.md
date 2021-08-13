---
title: Interfacce QMGR
description: Usare le interfacce di Gestione code (QMGR) seguenti per scaricare i file e monitorare i processi all'interno della coda di download.
ms.assetid: b5b59d4f-fa18-4225-8b6f-5d4033c61650
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a17bd3c27fad81416b916b52b055bc879b44f251113d43b6118e179b609762fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118679995"
---
# <a name="qmgr-interfaces"></a>Interfacce QMGR

\[Le interfacce di Gestione code (QMGR) sono disponibili per l'uso nei sistemi operativi specificati nella sezione Requisiti di un argomento. Possono essere modificati o non disponibili nelle versioni successive. Usare invece le [interfacce BITS](bits-interfaces.md).\]

Usare le interfacce di Gestione code (QMGR) seguenti per scaricare i file e monitorare i processi all'interno della coda di download.



| Interfaccia                                                                 | Descrizione                                                                                                                                                   |
|---------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IBackgroundCopyCallback1**](/windows/desktop/api/Qmgr/nn-qmgr-ibackgroundcopycallback1)<br/>   | Implementare per ricevere una notifica quando si verificano eventi.<br/>                                                                                               |
| [**IBackgroundCopyGroup**](/windows/desktop/api/Qmgr/nn-qmgr-ibackgroundcopygroup)<br/>           | Usare per gestire il gruppo. Ad esempio, aggiungere un processo al gruppo, impostare le proprietà del gruppo e avviare e arrestare il gruppo nella coda di download.<br/> |
| [**IBackgroundCopyJob1**](/windows/desktop/api/Qmgr/nn-qmgr-ibackgroundcopyjob1)<br/>             | Usare per aggiungere file al processo e recuperare lo stato del processo.<br/>                                                                                         |
| [**IBackgroundCopyQMgr**](/windows/desktop/api/Qmgr/nn-qmgr-ibackgroundcopyqmgr)<br/>             | Usare per creare un nuovo gruppo, recuperare un gruppo esistente o enumerare tutti i gruppi nella coda.<br/>                                                       |
| [**IEnumBackgroundCopyGroups**](/windows/desktop/api/Qmgr/nn-qmgr-ienumbackgroundcopygroups)<br/> | Usare per recuperare un elenco di gruppi nella coda di download.<br/>                                                                                            |
| [**IEnumBackgroundCopyJobs1**](/windows/desktop/api/Qmgr/nn-qmgr-ienumbackgroundcopyjobs1)<br/>   | Usare per recuperare un elenco di processi nel gruppo.<br/>                                                                                                       |



 

 

 





