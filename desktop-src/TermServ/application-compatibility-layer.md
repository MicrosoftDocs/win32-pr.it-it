---
title: Livello di compatibilità delle applicazioni
description: Per eseguire applicazioni legacy in un ambiente Servizi Desktop remoto è possibile usare il Servizi Desktop remoto livello di compatibilità delle applicazioni.
ms.assetid: 6e61ed45-4fcb-4aee-b8cc-638a9b87ce00
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3e7bbc5867e42951783d3666aa770cdcc45406f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300248"
---
# <a name="application-compatibility-layer"></a>Livello di compatibilità delle applicazioni

Per eseguire applicazioni legacy in un ambiente Servizi Desktop remoto è possibile usare il Servizi Desktop remoto livello di compatibilità delle applicazioni. Quando il server host sessione Desktop remoto (host sessione Desktop remoto) carica un'applicazione non Servizi Desktop remoto compatibile, carica anche una DLL che contiene il codice di compatibilità. Per utilizzare il livello di compatibilità dell'applicazione Servizi Desktop remoto, è possibile impostare il flag NOT TSAWARE durante la compilazione di un'applicazione.

Se l'applicazione è Servizi Desktop remoto consapevole, è possibile evitare il sovraccarico dovuto al caricamento di questa DLL aggiuntiva e all'esecuzione del codice di compatibilità.

Per indicare che l'applicazione è Servizi Desktop remoto in grado di riconoscere, impostare il flag DLLCHARACTERISTICS per l' **immagine di \_ \_ Terminal \_ server \_** nell'intestazione facoltativa. Se si usa il linker fornito con Microsoft Visual C++, è possibile usare l'opzione del linker **TSAWARE** per impostare questo flag. Lo strumento **dumpbin** fornito con Microsoft Visual C++ fornisce l'opzione */headers* per determinare lo stato del flag **TSAWARE** . Per ulteriori informazioni sull'utilizzo dello strumento **dumpbin** , vedere [riferimenti a DUMPBIN](/cpp/build/reference/dumpbin-reference?view=vs-2019).

Prestare attenzione quando si usa il flag **TSAWARE** , in quanto consente all'applicazione di ignorare eventuali ottimizzazioni per la compatibilità Servizi Desktop remoto. Il flag **TSAWARE** deve essere usato solo se si è certi che l'applicazione sia progettata per l'ambiente Servizi Desktop remoto. Se l'applicazione soddisfa i criteri seguenti, è possibile usare in modo sicuro il flag **\_ DLLCHARACTERISTICS di \_ Terminal \_ server \_** per le immagini.

-   L'applicazione non utilizza file ini.
-   L'applicazione non scrive in **HKEY l' \_ \_ utente corrente** durante l'installazione. Per ulteriori informazioni, vedere [archiviazione delle informazioni di User-Specific](storing-user-specific-information.md).
-   L'applicazione non viene eseguita come servizio di sistema (ovvero, LUID = System).
-   L'applicazione non prevede l'accesso esclusivo alle finestre o ad altre directory di sistema. Ciò significa che l'applicazione non archivia i dati temporanei o di configurazione per utente in Windows o in altre directory di sistema.
-   L'applicazione non scrive nell'hive del registro di sistema del **computer locale HKEY** per la configurazione o i dati specifici dell'utente.
-   L'applicazione segue le altre linee guida sulla compatibilità Servizi Desktop remoto citate in questo documento.

 

 