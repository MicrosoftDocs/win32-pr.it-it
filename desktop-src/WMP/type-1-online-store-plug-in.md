---
title: Digitare 1 plug-in di archivio online
description: Digitare 1 plug-in di archivio online
ms.assetid: 3aa74282-522b-4240-8d72-73bd3015abeb
keywords:
- Windows Media Player Online Stores, plug-in
- archivi online, plug-in
- digitare 1 negozi online, plug-in
- Windows Media Player Online Stores, interfaccia IWMPContentPartner
- negozi online, interfaccia IWMPContentPartner
- tipo 1 Store online, interfaccia IWMPContentPartner
- plug-in, archivi Windows Media Player online
- plug-in, archivi online
- plug-in, digitare 1 negozi online
- plug-in, interfaccia IWMPContentPartner
- Plug-in di Windows Media Player, digitare 1 negozi online
- Plug-in di Windows Media Player, archivi online
- Plug-in di Windows Media Player, archivi Windows Media Player online
- Plug-in di Windows Media Player, interfaccia IWMPContentPartner
- IWMPContentPartner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fe42095d08262520734603a5418ac6831ce6685
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "104046444"
---
# <a name="type-1-online-store-plug-in"></a>Digitare 1 plug-in di archivio online

Per sfruttare i vantaggi delle funzionalità di integrazione delle librerie, è necessario che i provider di archivio online di tipo 1 creino un plug-in che implementi l'interfaccia [IWMPContentPartner](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner) . Questa interfaccia fornisce i metodi che Windows Media Player chiama per inviare una notifica al negozio online sulle attività eseguite nel lettore e recuperare informazioni specifiche sul contenuto del negozio online, sul catalogo o sull'archivio.

Dopo che Windows Media Player crea un'istanza del plug-in, il lettore chiama [IWMPContentPartner:: filecallback](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-setcallback)e fornisce un puntatore all'interfaccia **IWMPContentPartnerCallback** . Questa interfaccia consente al negozio online di effettuare chiamate a Windows Media Player per fornire informazioni sullo stato o per avviare processi specifici, ad esempio il download di un brano musicale.

Windows Media Player e il plug-in vengono eseguiti in processi distinti. Il plug-in è un server in-process eseguito nel surrogato predefinito della DLL, dllhost.exe.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni sugli archivi online di tipo 1**](about-type-1-online-stores.md)
</dt> <dt>

[**Interfaccia IWMPContentPartner**](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner)
</dt> <dt>

[**Interfaccia IWMPContentPartnerCallback**](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartnercallback)
</dt> </dl>

 

 




