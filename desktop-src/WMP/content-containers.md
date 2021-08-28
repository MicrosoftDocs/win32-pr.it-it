---
title: Contenitori di contenuto
description: Contenitori di contenuto
ms.assetid: bed0293b-4765-4d1b-861c-f0c0a064df5f
keywords:
- Windows Media Player online, contenitori di contenuto
- negozi online, contenitori di contenuto
- tipo 1 negozi online, contenitori di contenuto
- Windows Media Player store online, interfaccia IWMPContentContainer
- negozi online, interfaccia IWMPContentContainer
- tipo 1 negozi online, interfaccia IWMPContentContainer
- Windows Media Player, contenitori di contenuto
- Windows Media Player,Interfaccia IWMPContentContainer
- contenitori di contenuto
- IWMPContentContainer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c582a04bd37e54a40f952402343c09fb7243fc07377ef7f507cc76f11390357c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123681"
---
# <a name="content-containers"></a>Contenitori di contenuto

Windows Media Player i contenitori di contenuto per rappresentare il contenuto multimediale digitale in una transazione di download o acquisto di una sottoscrizione. Un contenitore di contenuto è rappresentato **dall'interfaccia IWMPContentContainer.** Un contenitore di contenuto può contenere un elenco di contenuto correlato, ad esempio un album, un set di elementi di contenuto non correlato o *tiene traccia di*. È possibile usare **l'interfaccia IWMPContentContainer** per enumerare le tracce del contenitore di contenuto e recuperare il prezzo di ogni traccia. È anche possibile recuperare informazioni sul contenitore di contenuto stesso, ad esempio l'ID del contenitore, il tipo di contenuto nel contenitore e il prezzo totale per le tracce nel contenitore (che potrebbe differire dalla somma dei prezzi delle singole tracce, come nel caso di un acquisto di album).

Per fornire un meccanismo per la creazione di pacchetti di più contenitori di contenuto in un singolo Windows Media Player supporta **l'interfaccia IWMPContentContainerList.** **IWMPContentContainerList fornisce** metodi per enumerare e recuperare i contenitori di contenuto nell'elenco. Per scoprire se l'elenco di contenitori di contenuti rappresenta un acquisto o un download di sottoscrizione, chiamare [IWMPContentContainerList::GetTransactionType](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentcontainerlist-gettransactiontype) per recuperare un [valore WMPTransactionType.](/previous-versions/windows/desktop/api/contentpartner/ne-contentpartner-wmptransactiontype)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni sui negozi online di tipo 1**](about-type-1-online-stores.md)
</dt> <dt>

[**Interfaccia IWMPContentContainer**](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentcontainer)
</dt> <dt>

[**Interfaccia IWMPContentContainerList**](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentcontainerlist)
</dt> </dl>

 

 




