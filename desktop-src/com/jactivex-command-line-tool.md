---
title: Strumento di Command-Line JActiveX
description: L'applicazione della riga di comando JActiveX è un componente di Visual J++ 6.0.
ms.assetid: b356eb85-5dd4-475b-8d53-8c13a84aa976
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae611e56c44b78398817cd0c78804d343fa97754f80fb3b036ea2705c801070f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992651"
---
# <a name="jactivex-command-line-tool"></a>Strumento di Command-Line JActiveX

L'applicazione della riga di comando JActiveX è un componente di Visual J++ 6.0. Legge la libreria dei tipi di un controllo microsoft ActiveX e genera i file di origine Java corrispondenti. È quindi possibile compilare questi file di origine e importarli nell'applicazione Java.

Per generare file di origine Java per un oggetto COM, dal prompt dei comandi eseguire:

**nome file jactivex** 

dove *nomefile* è il nome del file che contiene la libreria dei tipi. Questo file può avere una delle estensioni di file seguenti: tlb, olb, ocx, .dll o .exe.

Per altre informazioni sui parametri facoltativi che è possibile impostare in JActiveX, vedere la documentazione di Visual J++ o digitare la riga di comando seguente:

**jactivex /?**

> [!WARNING]
> Non usare compilatori Visual J++ precedenti alla versione 1.02.3920 per compilare i file generati da JActiveX.exe. Ciò è dovuto al fatto che i file di origine generati devono essere compilati con un @com-aware compilatore. Solo i compilatori Visual J++ successivi alla versione 1.02.3920 sono @com-aware .

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Traduzione in Java](translating-to-java.md)
</dt> </dl>

 

 




