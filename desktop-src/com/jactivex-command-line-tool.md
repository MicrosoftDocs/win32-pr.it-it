---
title: Strumento Command-Line JActiveX
description: L'applicazione della riga di comando JActiveX è un componente di Visual J++ 6,0.
ms.assetid: b356eb85-5dd4-475b-8d53-8c13a84aa976
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9975e060a3967f927440111719045378aa812f16
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298937"
---
# <a name="jactivex-command-line-tool"></a>Strumento Command-Line JActiveX

L'applicazione della riga di comando JActiveX è un componente di Visual J++ 6,0. Viene letta la libreria dei tipi di un controllo Microsoft ActiveX e vengono generati i file di origine Java corrispondenti. È quindi possibile compilare questi file di origine e importarli nell'applicazione Java.

Per generare file di origine Java per un oggetto COM, dal prompt dei comandi eseguire:

 *nome file* JActiveX

dove *filename* è il nome del file che contiene la libreria dei tipi. Questo file può avere una delle seguenti estensioni di file:. tlb,. olb,. ocx,. dll o. exe.

Per ulteriori informazioni sui parametri facoltativi che è possibile impostare in JActiveX, vedere la documentazione di Visual J++ oppure digitare la seguente riga di comando:

**JActiveX/?**

> [!WARNING]
> Non usare i compilatori Visual J++ prima della versione 1.02.3920 per compilare i file generati da JActiveX.exe. Questo perché i file di origine generati devono essere compilati con un @com-aware compilatore. Solo i compilatori di Visual J++ successivi alla versione 1.02.3920 sono @com-aware .

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Conversione in Java](translating-to-java.md)
</dt> </dl>

 

 




