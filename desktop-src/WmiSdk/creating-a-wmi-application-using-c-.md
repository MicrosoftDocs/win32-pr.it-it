---
description: "Per creare un'applicazione per WMI con C++: è necessario inizializzare COM, accedere e impostare i protocolli WMI ed eseguire una pulizia manuale."
ms.assetid: 0b9b7990-6982-4ba9-8dba-7470990405f7
ms.tgt_platform: multiple
title: Creazione di un'applicazione WMI con C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fc68bfb9b7c17967de3142c3e431b51fc340a32acfb94484030e8fe744bf067
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612401"
---
# <a name="creating-a-wmi-application-using-c"></a>Creazione di un'applicazione WMI con C++

Per creare un'applicazione per WMI con C++: è necessario inizializzare COM, accedere e impostare i protocolli WMI ed eseguire una pulizia manuale. Tuttavia, C++ offre il vantaggio della flessibilità e della potenza. Pertanto, anche se si è meglio serviti nell'uso di Visual Basic Scripting Edition (VBScript) o Windows PowerShell per processi semplici, C++ funziona meglio per applicazioni più sofisticate ed è necessario per la scrittura di [provider](providing-data-to-wmi.md).

La procedura seguente descrive come creare un'applicazione WMI.

**Per creare un'applicazione WMI**

1.  [Inizializzare COM](initializing-com-for-a-wmi-application.md).

    Poiché WMI è basato sulla tecnologia COM, è necessario eseguire chiamate alle [**funzioni CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) e [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) per accedere a WMI.

2.  [Creare una connessione a uno spazio dei nomi WMI](creating-a-connection-to-a-wmi-namespace.md).

    Per definizione, WMI viene eseguito in un processo diverso da quello dell'applicazione. Pertanto, è necessario creare una connessione tra l'applicazione e WMI.

3.  [Impostare i livelli di sicurezza per la connessione WMI.](setting-the-security-levels-on-a-wmi-connection.md)

    Per usare la connessione creata a WMI, è necessario impostare i livelli di rappresentazione e autenticazione per l'applicazione.

4.  Implementare lo scopo dell'applicazione.

    WMI espone un'ampia gamma di interfacce COM usate per accedere ai dati e modificarli nell'azienda. Per altre informazioni, vedere [Modifica delle informazioni su classi e istanze](manipulating-class-and-instance-information.md), Ricezione di un evento [WMI](receiving-a-wmi-event.md)e API COM [per WMI](com-api-for-wmi.md).

    È qui che deve esistere la maggior parte dell'applicazione client WMI, ad esempio l'accesso a oggetti WMI o la modifica dei dati.

5.  [Pulire e arrestare l'applicazione](cleaning-up-and-shutting-down-a-wmi-application.md).

    Dopo aver completato le query in WMI, è necessario eliminare tutti i puntatori COM e arrestare correttamente l'applicazione.

Per altre informazioni e un esempio di codice su come creare un'applicazione WMI, vedere [Esempio: Creazione di un'applicazione WMI](example-creating-a-wmi-application.md).

 

 
