---
description: Contiene il metodo utilizzato per ottenere un endpoint usato per connettersi a un servizio.
ms.assetid: 4380776A-3B89-444B-B1E9-DCF640D0AEB4
title: Interfaccia IUpdateEndpointProvider
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointProvider
api_type:
- COM
ms.openlocfilehash: 2242e30ccd64c0252d5a1ea97eedd865f9e80bee2c58f749ca6d2eabd64c6167
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119896841"
---
# <a name="iupdateendpointprovider-interface"></a>Interfaccia IUpdateEndpointProvider

Contiene il metodo utilizzato per ottenere un endpoint usato per connettersi a un servizio. Questa interfaccia viene implementata durante la scrittura di un provider di endpoint.

## <a name="members"></a>Membri

**L'interfaccia IUpdateEndpointProvider** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IUpdateEndpointProvider** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

Questi metodi sono disponibili nell'interfaccia **IUpdateEndpointProvider.**



| Metodo                                                                       | Descrizione                                                           |
|:-----------------------------------------------------------------------------|:----------------------------------------------------------------------|
| [**GetServiceEndpoint**](iupdateendpointauthprovider-getserviceendpoint.md) | Richiede un endpoint usato per connettersi a un servizio.<br/> |



 

## <a name="remarks"></a>Commenti

WUA chiama il [**metodo GetServiceEndpoint**](iupdateendpointauthprovider-getserviceendpoint.md) per avviare il processo di negoziazione. Quando viene effettuata la chiamata, WUA passa i tipi di token registrati e l'implementazione di questa interfaccia restituisce i tipi di token che preferisce usare.

 

 
