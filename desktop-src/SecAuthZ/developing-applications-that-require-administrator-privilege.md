---
description: È possibile sviluppare un'applicazione che esegue operazioni che richiedono privilegi di amministratore ma che vengono eseguite come utente standard.
ms.assetid: 78099b59-b09b-43c0-91f5-adb5c9e0e191
title: Sviluppo di applicazioni che richiedono privilegi di amministratore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 410dc8ea112cfec6297cf7c11a044e62695a24e93d7eb0b13a773d40acd6c6cc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119994431"
---
# <a name="developing-applications-that-require-administrator-privilege"></a>Sviluppo di applicazioni che richiedono privilegi di amministratore

È possibile sviluppare un'applicazione che esegue operazioni che richiedono privilegi di amministratore ma che vengono eseguite come utente standard.

Esistono diversi modelli per eseguire questa operazione.



| Argomento                                                                | Descrizione                                                                                                                                                                                          |
|----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Modello di attività con privilegi elevati](elevated-task-model.md)                       | Un'applicazione in esecuzione come utente standard esegue operazioni che richiedono privilegi di amministratore avviando un'attività pianificata.                                                                     |
| [Modello di servizio del sistema operativo](operating-system-service-model.md) | Un'applicazione in esecuzione come utente standard comunica con un servizio in esecuzione come **SYSTEM** tramite [RPC (Remote Procedure Call).](/windows/desktop/Rpc/rpc-start-page)                                              |
| [Modello broker amministratore](administrator-broker-model.md)         | L'applicazione è suddivisa in due programmi. Uno dei programmi viene eseguito come utente standard e l'altro viene eseguito con privilegi di amministratore.                                                          |
| [Modello a oggetti COM administrator](administrator-com-object-model.md) | Un'applicazione in esecuzione come utente standard esegue operazioni che richiedono privilegi di amministratore creando un oggetto Component Object Model [con](/windows/desktop/com/component-object-model--com--portal) privilegi elevati. |



 

 

 
