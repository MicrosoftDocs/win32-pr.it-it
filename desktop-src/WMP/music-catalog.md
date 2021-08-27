---
title: Musica Catalogo
description: Musica Catalogo
ms.assetid: d7ebf37f-00ae-4978-a63d-9d13741724f5
keywords:
- Windows Media Player online, cataloghi musicali
- negozi online, cataloghi musicali
- store online di tipo 1, cataloghi musicali
- Windows Media Player negozi online, compilatore del catalogo
- negozi online, compilatore di catalogo
- tipo 1 negozi online, compilatore di catalogo
- cataloghi musicali
- compilatore catalog
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2474204686a498c81ec12b87daeba99f21397492dc5178a70580d4a37750d9cd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123301"
---
# <a name="music-catalog"></a>Musica Catalogo

Un negozio online di tipo 1 crea il catalogo musicale come set di file TSV (Tab Separated Value). Lo store online usa [](catalog-compiler-for-type-1-online-stores.md) quindi il compilatore del catalogo di Microsoft per compilare i file TSV in un catalogo compresso che può essere scaricato Windows Media Player. Windows Media Player possibile scaricare i file di catalogo completi o i file di aggiornamento del catalogo. Gli aggiornamenti del catalogo contengono solo le informazioni del catalogo modificate dopo l'ultimo aggiornamento del catalogo. Il plug-in partner per i contenuti deve determinare se scaricare un catalogo completo o un aggiornamento. In entrambi i casi, Windows Media Player le modifiche al catalogo corrente al momento della notifica dal plug-in.

Se lo store online ha preparato un nuovo catalogo, il plug-in può inviare una notifica al lettore chiamando [IWMPContentPartnerCallback::Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify) e passando wmpcnNewCatalogAvailable come valore per il parametro *di* tipo.

Quando Windows Media Player è pronto per scaricare un catalogo o un aggiornamento, il lettore chiama [IWMPContentPartner::GetCatalogURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl). Questo metodo fornisce al plug-in informazioni sul catalogo corrente, ad esempio la versione del catalogo e l'identificatore delle impostazioni locali. Il plug-in risponde fornendo l'URL (Uniform Resource Locator) del catalogo o dell'aggiornamento completo corretto, nonché un numero di versione aggiornato e una data di scadenza. Windows Media Player richiederà periodicamente gli aggiornamenti del catalogo in base alle informazioni fornite dal plug-in in **GetCatalogURL**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni sui negozi online di tipo 1**](about-type-1-online-stores.md)
</dt> <dt>

[**Compilatore del catalogo per i negozi online di tipo 1**](catalog-compiler-for-type-1-online-stores.md)
</dt> <dt>

[**Interfaccia IWMPContentPartner**](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner)
</dt> </dl>

 

 




