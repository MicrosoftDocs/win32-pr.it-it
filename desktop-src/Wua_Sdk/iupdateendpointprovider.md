---
description: Contiene il metodo utilizzato per ottenere un endpoint utilizzato per connettersi a un servizio.
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
ms.openlocfilehash: 81e9481f5233fac05e7fa7bdf3afa53c4c55513a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307614"
---
# <a name="iupdateendpointprovider-interface"></a>Interfaccia IUpdateEndpointProvider

Contiene il metodo utilizzato per ottenere un endpoint utilizzato per connettersi a un servizio. Questa interfaccia viene implementata quando si scrive un provider di endpoint.

## <a name="members"></a>Membri

L'interfaccia **IUpdateEndpointProvider** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IUpdateEndpointProvider** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IUpdateEndpointProvider** dispone di questi metodi.



| Metodo                                                                       | Descrizione                                                           |
|:-----------------------------------------------------------------------------|:----------------------------------------------------------------------|
| [**Getserviceendpoint**](iupdateendpointauthprovider-getserviceendpoint.md) | Richiede un endpoint utilizzato per connettersi a un servizio.<br/> |



 

## <a name="remarks"></a>Commenti

WUA chiama il metodo [**getserviceendpoint**](iupdateendpointauthprovider-getserviceendpoint.md) per avviare il processo di negoziazione. Quando viene effettuata la chiamata, WUA passa i tipi di token registrati e l'implementazione di questa interfaccia restituisce i tipi di token che preferisce usare.

 

 
