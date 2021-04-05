---
title: Strumento Command-Line JavaTLB
description: Strumento Command-Line JavaTLB
ms.assetid: b46d7bcc-ccd9-4242-9b19-f398d2cb8f91
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7a0214648f7ad86613d6b35e3084021e2be24aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714428"
---
# <a name="javatlb-command-line-tool"></a>Strumento Command-Line JavaTLB

JavaTLB è un componente di Visual J++ 5,0. JavaTLB è un'applicazione della riga di comando che genera file di classe per un oggetto COM. I metodi che contengono tipi di dati che non possono essere rappresentati in modo accurato e sicuro in Java non vengono convertiti.

Diversamente dalla [procedura guidata libreria dei tipi Java](java-type-library-wizard.md), JavaTLB non genera un file di riepilogo contenente le informazioni sulla libreria dei tipi Java.

Per generare file di classe Java per un singolo oggetto COM, dal prompt dei comandi eseguire:

 *nome file* JavaTLB

dove *filename* è il nome del file che contiene la libreria dei tipi. Questo file può avere una delle seguenti estensioni di file:. tlb,. olb,. ocx,. dll o. exe.

Per generare file di classe Java per più oggetti COM, dal prompt dei comandi eseguire:

**JavaTLB @ * * * TextFile*

dove *TextFile* è il nome di un file di testo contenente un elenco dei file contenenti le librerie dei tipi dell'oggetto com.

> [!Note]  
> In Visual J++ 6,0 lo strumento da riga di comando JavaTLB viene sostituito dallo [strumento JActiveX](jactivex-command-line-tool.md). Per ulteriori informazioni, vedere la documentazione di Visual J++ 6,0.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Conversione in Java](translating-to-java.md)
</dt> </dl>

 

 




