---
title: Contenitori di contenuto
description: Contenitori di contenuto
ms.assetid: bed0293b-4765-4d1b-861c-f0c0a064df5f
keywords:
- Windows Media Player Online Stores, contenitori di contenuti
- archivi online, contenitori di contenuti
- digitare 1 negozi online, contenitori di contenuto
- Windows Media Player Online Stores, interfaccia IWMPContentContainer
- negozi online, interfaccia IWMPContentContainer
- tipo 1 Store online, interfaccia IWMPContentContainer
- Windows Media Player, contenitori di contenuto
- Windows Media Player, interfaccia IWMPContentContainer
- contenitori di contenuto
- IWMPContentContainer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 801816c3e26920f3d0869190fc1101d6017a524e
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/21/2020
ms.locfileid: "106299511"
---
# <a name="content-containers"></a>Contenitori di contenuto

Windows Media Player usa i contenitori di contenuto per rappresentare il contenuto multimediale digitale in un download o una transazione di acquisto della sottoscrizione. Un contenitore di contenuti è rappresentato dall'interfaccia **IWMPContentContainer** . Un contenitore di contenuto potrebbe contenere un elenco di contenuti correlati, ad esempio un album, o un set di elementi di contenuto non correlati o *tracce*. È possibile usare l'interfaccia **IWMPContentContainer** per enumerare le tracce del contenitore di contenuto e recuperare il prezzo di ogni traccia. È anche possibile recuperare informazioni sul contenitore di contenuto stesso, ad esempio l'ID del contenitore, il tipo di contenuto nel contenitore e il prezzo totale per le tracce nel contenitore (che potrebbero differire dalla somma dei prezzi delle singole tracce, come nel caso di un acquisto di album).

Per fornire un meccanismo per la creazione di pacchetti di più contenitori di contenuto in un singolo oggetto, Windows Media Player supporta l'interfaccia **IWMPContentContainerList** . **IWMPContentContainerList** fornisce metodi per enumerare e recuperare i contenitori di contenuto nell'elenco. Per individuare se l'elenco di contenitori di contenuto rappresenta un download di acquisto o di sottoscrizione, chiamare [IWMPContentContainerList:: GetTransactionType](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentcontainerlist-gettransactiontype) per recuperare un valore [WMPTransactionType](/previous-versions/windows/desktop/api/contentpartner/ne-contentpartner-wmptransactiontype) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni sugli archivi online di tipo 1**](about-type-1-online-stores.md)
</dt> <dt>

[**Interfaccia IWMPContentContainer**](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentcontainer)
</dt> <dt>

[**Interfaccia IWMPContentContainerList**](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentcontainerlist)
</dt> </dl>

 

 




