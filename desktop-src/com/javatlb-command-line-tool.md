---
title: Strumento di Command-Line JavaTLB
description: Strumento di Command-Line JavaTLB
ms.assetid: b46d7bcc-ccd9-4242-9b19-f398d2cb8f91
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0ade0a20a1c41310422c08310f2d0534914993d79909f51990c48aa04df0a5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117918625"
---
# <a name="javatlb-command-line-tool"></a>Strumento di Command-Line JavaTLB

JavaTLB è un componente di Visual J++ 5.0. JavaTLB è un'applicazione della riga di comando che genera file di classe per un oggetto COM. I metodi che contengono tipi di dati che non possono essere rappresentati in modo accurato e sicuro in Java non vengono convertiti.

A differenza [della Creazione guidata libreria dei tipi Java,](java-type-library-wizard.md)JavaTLB non genera un file di riepilogo contenente le informazioni sulla libreria dei tipi Java.

Per generare file di classe Java per un singolo oggetto COM, dal prompt dei comandi eseguire:

**nome file javatlb** 

dove *nomefile* è il nome del file che contiene la libreria dei tipi. Questo file può avere una delle estensioni di file seguenti: .tlb, .olb, .ocx, .dll o .exe.

Per generare file di classe Java per più oggetti COM, dal prompt dei comandi eseguire:

**javatlb @**_TextFile_

dove *TextFile* è il nome di un file di testo che contiene un elenco dei file contenenti le librerie dei tipi dell'oggetto COM.

> [!Note]  
> In Visual J++ 6.0 lo strumento da riga di comando JavaTLB viene sostituito dallo [strumento JActiveX](jactivex-command-line-tool.md). Per altre informazioni, vedere la documentazione di Visual J++ 6.0.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Traduzione in Java](translating-to-java.md)
</dt> </dl>

 

 




