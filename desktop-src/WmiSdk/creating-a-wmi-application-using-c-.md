---
description: "Per creare un'applicazione per WMI mediante C++: è necessario inizializzare COM, accedere e impostare i protocolli WMI ed eseguire una pulizia manuale."
ms.assetid: 0b9b7990-6982-4ba9-8dba-7470990405f7
ms.tgt_platform: multiple
title: Creazione di un'applicazione WMI con C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baaa4f7e79828b2cb6cb496254d906182ff611ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348406"
---
# <a name="creating-a-wmi-application-using-c"></a>Creazione di un'applicazione WMI con C++

Per creare un'applicazione per WMI mediante C++: è necessario inizializzare COM, accedere e impostare i protocolli WMI ed eseguire una pulizia manuale. Tuttavia, C++ ha il vantaggio di flessibilità e potenza. Pertanto, anche se è meglio utilizzare Visual Basic Scripting Edition (VBScript) o Windows PowerShell per semplici processi, C++ funziona meglio per applicazioni più sofisticate ed è necessario per la scrittura di [provider](providing-data-to-wmi.md).

Nella procedura riportata di seguito viene descritto come creare un'applicazione WMI.

**Per creare un'applicazione WMI**

1.  [Inizializzare com](initializing-com-for-a-wmi-application.md).

    Poiché WMI è basato sulla tecnologia COM, è necessario eseguire chiamate alle funzioni [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) e [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) per accedere a WMI.

2.  [Creare una connessione a uno spazio dei nomi WMI](creating-a-connection-to-a-wmi-namespace.md).

    Per definizione, WMI viene eseguito in un processo diverso rispetto all'applicazione. Pertanto, è necessario creare una connessione tra l'applicazione e WMI.

3.  [Impostare i livelli di sicurezza per la connessione WMI](setting-the-security-levels-on-a-wmi-connection.md).

    Per utilizzare la connessione creata a WMI, è necessario impostare i livelli di autenticazione e di rappresentazione per l'applicazione.

4.  Implementare lo scopo dell'applicazione.

    WMI espone un'ampia gamma di interfacce COM che consentono di accedere e modificare i dati nell'azienda. Per ulteriori informazioni, vedere [modifica delle informazioni di classe e istanza](manipulating-class-and-instance-information.md), [ricezione di un evento WMI](receiving-a-wmi-event.md)e [API com per WMI](com-api-for-wmi.md).

    Questo è il punto in cui deve esistere la maggior parte dell'applicazione client WMI, ad esempio l'accesso agli oggetti WMI o la manipolazione dei dati.

5.  [Pulire e arrestare l'applicazione](cleaning-up-and-shutting-down-a-wmi-application.md).

    Dopo aver completato le query in WMI, è necessario eliminare tutti i puntatori COM e arrestare correttamente l'applicazione.

Per ulteriori informazioni e un esempio di codice su come creare un'applicazione WMI, vedere [esempio: creazione di un'applicazione WMI](example-creating-a-wmi-application.md).

 

 
