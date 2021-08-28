---
title: Livello di compatibilità delle applicazioni
description: Per eseguire applicazioni legacy in un ambiente Servizi Desktop remoto è possibile usare il Servizi Desktop remoto di compatibilità delle applicazioni.
ms.assetid: 6e61ed45-4fcb-4aee-b8cc-638a9b87ce00
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c3630346578801e4d2578db6f528048914412dc9ad1a8544e2c2d303188814b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099611"
---
# <a name="application-compatibility-layer"></a>Livello di compatibilità delle applicazioni

Per eseguire applicazioni legacy in un ambiente Servizi Desktop remoto è possibile usare il Servizi Desktop remoto di compatibilità delle applicazioni. Quando il server Host sessione Desktop remoto (Host sessione Desktop remoto) carica un'applicazione che non è compatibile con Servizi Desktop remoto, carica anche una DLL che contiene codice di compatibilità. Per usare il Servizi Desktop remoto di compatibilità delle applicazioni, è possibile impostare il flag NOT TSAWARE durante la compilazione di un'applicazione.

Se l'applicazione è Servizi Desktop remoto, è possibile evitare l'overhead dovuto al caricamento di questa DLL aggiuntiva e all'esecuzione del codice di compatibilità.

Per indicare che l'applicazione è Servizi Desktop remoto, impostare il flag **IMAGE \_ DLLCHARACTERISTICS \_ TERMINAL SERVER \_ \_ AWARE** nell'intestazione facoltativa. Se si usa il linker fornito con Microsoft Visual C++, è possibile usare l'opzione del linker **TSAWARE** per impostare questo flag. Lo **strumento DUMPBIN** fornito con Microsoft Visual C++ l'opzione */HEADERS* per determinare lo stato del flag **TSAWARE.** Per altre informazioni sull'uso dello **strumento DUMPBIN,** vedere [DumpBIN Reference](/cpp/build/reference/dumpbin-reference?view=vs-2019).

Prestare attenzione quando si usa il flag **TSAWARE** perché consente all'applicazione di ignorare eventuali Servizi Desktop remoto di compatibilità. Il flag **TSAWARE** deve essere usato solo se si è certi che l'applicazione sia progettata per l'Servizi Desktop remoto ambiente. Se l'applicazione soddisfa i criteri seguenti, è possibile usare in modo sicuro il flag **IMAGE \_ DLLCHARACTERISTICS \_ TERMINAL SERVER \_ \_ AWARE.**

-   L'applicazione non usa .ini file.
-   L'applicazione non scrive in **HKEY \_ CURRENT USER \_ durante** l'installazione. Per altre informazioni, vedere [Archiviazione User-Specific informazioni](storing-user-specific-information.md).
-   L'applicazione non viene eseguita come servizio di sistema,ovvero LUID=System.
-   L'applicazione non prevede l'accesso esclusivo al Windows o ad altre directory di sistema. Ciò significa che l'applicazione non archivia i dati temporanei o di configurazione per utente nel Windows o in altre directory di sistema.
-   L'applicazione non scrive nell'hive del Registro di sistema del computer locale **HKEY** per la configurazione o i dati specifici dell'utente.
-   L'applicazione segue altre Servizi Desktop remoto sulla compatibilità indicate in questo documento.

 

 