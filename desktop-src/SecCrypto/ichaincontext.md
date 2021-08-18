---
description: Fornisce l'accesso al contesto di un oggetto CAPICOM Chain. Questo contesto consente l'uso della catena di attendibilità dei certificati CAPICOM in altre derivazioni di CryptoAPI.
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
ms.openlocfilehash: 5a3ac2f2234c986c9a86073e25e1277fa1af4f10f2809e013bc65849120b90c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005439"
---
# <a name="ichaincontext-interface"></a>Interfaccia IChainContext

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.\]

**L'interfaccia IChainContext** fornisce l'accesso al contesto di un oggetto [**CAPICOM Chain.**](chain.md) Questo contesto consente l'uso della catena di attendibilità dei certificati CAPICOM in altre derivazioni di CryptoAPI.

## <a name="when-to-use"></a>Utilizzo

Usare questa interfaccia quando è necessario usare un oggetto [**CapiCOM Chain**](chain.md) in un'altra derivazione di CryptoAPI.

## <a name="members"></a>Membri

**L'interfaccia IChainContext** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

**L'interfaccia IChainContext** include questi metodi.



| Metodo                                           | Descrizione                                                                                                                    |
|:-------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [**FreeContext**](ichaincontext-freecontext.md) | Rilascia un contesto PCCERT \_ CHAIN acquisito tramite la proprietà \_ [**ChainContext.**](ichaincontext-chaincontext.md)<br/> |



 

### <a name="properties"></a>Proprietà

**L'interfaccia IChainContext** ha queste proprietà.



| Proprietà                                                      | Tipo di accesso           | Descrizione                                                               |
|:--------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------|
| [**ChainContext**](ichaincontext-chaincontext.md)<br/> | Lettura/Scrittura<br/> | Imposta o recupera l'oggetto PCCERT \_ CHAIN CONTEXT di un \_ certificato.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 




