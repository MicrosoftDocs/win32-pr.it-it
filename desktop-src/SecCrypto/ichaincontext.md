---
description: Fornisce l'accesso al contesto di un oggetto chain di capico. Questo contesto consente l'uso della catena di certificati del certificato CAPICOM in altre derivazioni di CryptoAPI.
ms.assetid: ee258586-028e-486e-8129-07f43b6cc468
title: Interfaccia IChainContext
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IChainContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 34ba471c50ceb9475121139c3ecb997cf1d26f2b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106323966"
---
# <a name="ichaincontext-interface"></a>Interfaccia IChainContext

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.\]

L'interfaccia **IChainContext** fornisce l'accesso al contesto di un oggetto [**Chain**](chain.md) di capico. Questo contesto consente l'uso della catena di certificati del certificato CAPICOM in altre derivazioni di CryptoAPI.

## <a name="when-to-use"></a>Utilizzo

Usare questa interfaccia quando è necessario usare un oggetto [**catena**](chain.md) di CAPICOM in un'altra derivazione di CryptoAPI.

## <a name="members"></a>Membri

L'interfaccia **IChainContext** presenta questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'interfaccia **IChainContext** dispone di questi metodi.



| Metodo                                           | Descrizione                                                                                                                    |
|:-------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [**FreeContext**](ichaincontext-freecontext.md) | Rilascia un \_ \_ contesto della catena PCCERT acquisito tramite la proprietà [**chainContext**](ichaincontext-chaincontext.md) .<br/> |



 

### <a name="properties"></a>Proprietà

L'interfaccia **IChainContext** ha queste proprietà.



| Proprietà                                                      | Tipo di accesso           | Descrizione                                                               |
|:--------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------|
| [**ChainContext**](ichaincontext-chaincontext.md)<br/> | Lettura/Scrittura<br/> | Imposta o Recupera il \_ \_ contesto della catena PCCERT di un certificato.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 




