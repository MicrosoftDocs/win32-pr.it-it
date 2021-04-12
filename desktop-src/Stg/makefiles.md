---
title: Makefile
description: I makefile per ognuno degli esempi di codice di questa serie sono makefile generici Microsoft Win32 e devono essere creati dalla finestra del prompt dei comandi.
ms.assetid: f9944069-b536-4ae2-8411-f02c3a78978c
keywords:
- Archiviazione strutturata makefile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a15fef5818c28986232e8c2a648f43bdc096832f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332735"
---
# <a name="makefiles"></a>Makefile

I makefile per ognuno degli esempi di codice di questa serie sono makefile generici Microsoft Win32 e devono essere creati dalla finestra del prompt dei comandi. Si presuppone che gli strumenti del compilatore e del linker Microsoft e probabilmente dovranno essere modificati per lavorare con altri strumenti. La maggior parte delle opzioni della riga di comando del compilatore e del linker sono specificate dalle macro definite nel file di inclusione del makefile Win32. MAK incluso con la piattaforma Software Development Kit (SDK).

Il file di Makeall.bat e ogni rispettivo Makefile di esempio di codice supportano opzioni comuni, elencate nella tabella seguente, per la chiamata dalla finestra del prompt dei comandi per controllare la natura della compilazione.



| Chiamata a NMAKE        | Chiamata makeall          | Effetto                       |
|-------------------------|-----------------------------|------------------------------|
| **NMAKE**               | **makeall**                 | Compilare con le informazioni di debug.     |
| **NMAKE** **nodebug = 1** | **makeall** **"nodebug = 1"** | Compila senza informazioni di debug.  |
| profilo **NMAKE** **= 1** | **makeall** **"profile = 1"** | Compilare con le informazioni di profilatura. |
| ottimizzazione **NMAKE** **= 1**    | **makeall** **"Tune = 1"**    | Con working set informazioni sul sintonizzatore. |
| **NMAKE** **Unicode = 1** | **makeall** **"Unicode = 1"** | Compilare per Unicode.         |
|  **Pulisci** NMAKE     |  **Pulisci** makeall       | Elimina i file binari temporanei.   |
|  **cleanall** NMAKE  |  **cleanall** makeall    | Elimina tutti i file generati.  |



 

Per le chiamate di Makeall.bat è necessario avere le virgolette, come illustrato. Le opzioni **nodebug**, **profile** e **Tune** si escludono a vicenda: è possibile utilizzarne solo uno, o None, per una compilazione o un collegamento specifico. Per compilare gli esempi per l'esecuzione con stringhe Unicode, utilizzare l'opzione **"Unicode = 1"** . Per impostazione predefinita, la compilazione viene eseguita per il supporto delle stringhe ANSI tradizionali, in quanto è quindi possibile eseguire in qualsiasi sistema operativo Windows a 32 bit. È possibile compilare ed eseguire liberamente con o senza Unicode in Windows Server 2003 e versioni successive e Windows 2000 e versioni successive. Tenere presente che APPUTIL viene sempre compilato con le stesse opzioni degli altri esempi di codice che possono essere compilati separatamente. Questa operazione è particolarmente valida per l'opzione **"Unicode = 1"** .

È possibile usare un Integrated Development Environment C++ installato a 32 bit per compilare gli esempi usando i makefile generici forniti. A tale scopo, è necessario che all'interno dell'IDE i makefile generici vengano gestiti come Makefile "esterni". I makefile forniti richiedono un'utilità di make compatibile con Microsoft NMAKE.

La maggior parte degli IDE C++ è in grado di riconoscere questi makefile come esterni e fornisce comunque molti vantaggi di modifica-compilazione-debug dell'IDE. Ad esempio, in Microsoft Visual Studio 97 o versioni successive, è possibile usare il menu file scelta area di lavoro per produrre un'area di lavoro aprendo una copia denominata in modo appropriato (ad esempio, Exeskel. MAK) del makefile di esempio di codice Win32.

 

 




