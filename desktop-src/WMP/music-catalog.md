---
title: Catalogo musica
description: Catalogo musica
ms.assetid: d7ebf37f-00ae-4978-a63d-9d13741724f5
keywords:
- Windows Media Player Online Stores, cataloghi musica
- archivi online, cataloghi musicali
- digitare 1 negozi online, cataloghi musica
- Windows Media Player Online Stores, compilatore catalog
- archivi online, compilatore di cataloghi
- digitare 1 negozi online, compilatore di cataloghi
- Cataloghi musica
- compilatore Catalogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 479a74393ee4d853f591cb6d75eef8be741c9228
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104046278"
---
# <a name="music-catalog"></a>Catalogo musica

Un archivio online di tipo 1 crea il proprio catalogo musicale come un set di file con valori delimitati da tabulazioni (TSV). Quindi, il negozio online usa il [compilatore del catalogo](catalog-compiler-for-type-1-online-stores.md) Microsoft per compilare i file TSV in un catalogo compresso che può essere scaricato da Windows Media Player. Windows Media Player può scaricare i file di catalogo completi o i file di aggiornamento del catalogo. Gli aggiornamenti del catalogo contengono solo le informazioni sul catalogo modificate dopo l'ultimo aggiornamento del catalogo. È il plug-in del partner di contenuti a determinare se scaricare un catalogo completo o un aggiornamento. In entrambi i casi, Windows Media Player applica le modifiche al catalogo corrente al momento della notifica dal plug-in.

Se per l'archivio online è stato preparato un nuovo catalogo, il plug-in può inviare una notifica al lettore chiamando [IWMPContentPartnerCallback:: Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify) e passando wmpcnNewCatalogAvailable come valore per il parametro di *tipo* .

Quando Windows Media Player è pronto per il download di un catalogo o di un aggiornamento, il lettore chiama [IWMPContentPartner:: GetCatalogURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl). Questo metodo fornisce il plug-in con informazioni sul catalogo corrente, ad esempio la versione del catalogo e l'identificatore delle impostazioni locali. Il plug-in risponde fornendo l'URL (Uniform Resource Locator) del catalogo o dell'aggiornamento completo corretto, nonché un numero di versione e una data di scadenza aggiornati. Windows Media Player richiede periodicamente aggiornamenti del catalogo in base alle informazioni fornite dal plug-in in **GetCatalogURL**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni sugli archivi online di tipo 1**](about-type-1-online-stores.md)
</dt> <dt>

[**Compilatore del catalogo per i negozi di tipo 1 online**](catalog-compiler-for-type-1-online-stores.md)
</dt> <dt>

[**Interfaccia IWMPContentPartner**](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner)
</dt> </dl>

 

 




