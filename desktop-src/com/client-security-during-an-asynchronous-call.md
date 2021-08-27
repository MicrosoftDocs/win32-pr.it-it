---
title: Sicurezza client durante una chiamata asincrona
description: Sicurezza client durante una chiamata asincrona
ms.assetid: 26d1f2c2-cb08-49f1-8beb-b99b029f0d8c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c4c25e17712d0164938f3de9895d1e6b02582f2d86cba9957297e23aa4e7f1c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071041"
---
# <a name="client-security-during-an-asynchronous-call"></a>Sicurezza client durante una chiamata asincrona

La gestione proxy creata da MIDL per gli oggetti che usano il marshalling standard implementa [**l'interfaccia IClientSecurity.**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) I client possono gestire la sicurezza delle chiamate con marshalling effettuando una query per **IClientSecurity sull'oggetto** chiamata e ottenendo o modificando le impostazioni di sicurezza.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esecuzione di una chiamata asincrona](making-an-asynchronous-call.md)
</dt> </dl>

 

 




