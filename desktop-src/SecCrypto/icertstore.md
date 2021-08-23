---
description: Fornisce l'accesso al contesto di un oggetto CAPICOM Store. Questo contesto consente l'uso dell'archivio certificati CAPICOM in altre derivazioni di CryptoAPI.
ms.assetid: dc108e2d-d6ec-4972-9c8e-e6e738c25756
title: Interfaccia ICertStore
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertStore
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a48913b4bfb1fc28b612437a8f3b6934941c19b22683913f68d59f3f11d9e1c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005579"
---
# <a name="icertstore-interface"></a>Interfaccia ICertStore

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.\]

**L'interfaccia ICertStore** consente di accedere al contesto di un oggetto CAPICOM [**Store.**](store.md) Questo contesto consente l'uso dell'archivio certificati CAPICOM in altre derivazioni di CryptoAPI.

## <a name="when-to-use"></a>Utilizzo

Usare questa interfaccia quando è necessario usare un oggetto capiCOM [**Store**](store.md) in un'altra derivazione di CryptoAPI.

## <a name="members"></a>Membri

**L'interfaccia ICertStore** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

**L'interfaccia ICertStore** include questi metodi.



| Metodo                                        | Descrizione                                                                                                         |
|:----------------------------------------------|:--------------------------------------------------------------------------------------------------------------------|
| [**Closehandle**](icertstore-closehandle.md) | Chiude un handle HCERTSTORE acquisito tramite la [**proprietà StoreHandle.**](icertstore-storehandle.md)<br/> |



 

### <a name="properties"></a>Proprietà

**L'interfaccia ICertStore** ha queste proprietà.



| Proprietà                                                     | Tipo di accesso           | Descrizione                                                                                                         |
|:-------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------|
| [**StoreHandle**](icertstore-storehandle.md)<br/>     | Lettura/Scrittura<br/> | Imposta o recupera l'handle HCERTSTORE di un archivio certificati.<br/>                                          |
| [**StoreLocation**](icertstore-storelocation.md)<br/> | Lettura/Scrittura<br/> | Imposta o recupera l'archivio [**CAPICOM \_ \_ LOCATION**](capicom-store-location.md) di un archivio certificati.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 




