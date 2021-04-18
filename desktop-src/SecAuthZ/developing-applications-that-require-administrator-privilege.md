---
description: È possibile sviluppare un'applicazione che esegua operazioni che richiedono un privilegio di amministratore ancora eseguito come utente standard.
ms.assetid: 78099b59-b09b-43c0-91f5-adb5c9e0e191
title: Sviluppo di applicazioni che richiedono privilegi di amministratore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84d22687dad0a8914c5dcaebe8ea85a525529a34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315838"
---
# <a name="developing-applications-that-require-administrator-privilege"></a>Sviluppo di applicazioni che richiedono privilegi di amministratore

È possibile sviluppare un'applicazione che esegua operazioni che richiedono un privilegio di amministratore ancora eseguito come utente standard.

Sono disponibili diversi modelli per eseguire questa operazione.



| Argomento                                                                | Descrizione                                                                                                                                                                                          |
|----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Modello di attività con privilegi elevati](elevated-task-model.md)                       | Un'applicazione in esecuzione come utente standard esegue operazioni che richiedono privilegi di amministratore avviando un'attività pianificata.                                                                     |
| [Modello di servizio del sistema operativo](operating-system-service-model.md) | Un'applicazione in esecuzione come utente standard comunica con un servizio eseguito come **sistema** utilizzando RPC ( [Remote Procedure Call](/windows/desktop/Rpc/rpc-start-page) ).                                              |
| [Modello di broker amministratore](administrator-broker-model.md)         | L'applicazione è divisa in due programmi. Uno dei programmi viene eseguito come utente standard e l'altro viene eseguito con privilegi di amministratore.                                                          |
| [Modello a oggetti COM dell'amministratore](administrator-com-object-model.md) | Un'applicazione in esecuzione come utente standard esegue operazioni che richiedono privilegi di amministratore creando un oggetto [Component Object Model](/windows/desktop/com/component-object-model--com--portal) con privilegi elevati. |



 

 

 
