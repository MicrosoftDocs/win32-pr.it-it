---
description: Consente di accedere al contesto di un oggetto archivio CAPICOM. Questo contesto consente l'uso dell'archivio certificati CAPICOM in altre derivazioni di CryptoAPI.
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
ms.openlocfilehash: 119609399709340049bc43693ac51f6259021416
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328596"
---
# <a name="icertstore-interface"></a>Interfaccia ICertStore

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.\]

L'interfaccia **ICertStore** consente di accedere al contesto di un oggetto [**Archivio**](store.md) CAPICOM. Questo contesto consente l'uso dell'archivio certificati CAPICOM in altre derivazioni di CryptoAPI.

## <a name="when-to-use"></a>Utilizzo

Usare questa interfaccia quando è necessario usare un oggetto [**Archivio**](store.md) CAPICOM in un'altra derivazione di CryptoAPI.

## <a name="members"></a>Membri

L'interfaccia **ICertStore** presenta questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'interfaccia **ICertStore** dispone di questi metodi.



| Metodo                                        | Descrizione                                                                                                         |
|:----------------------------------------------|:--------------------------------------------------------------------------------------------------------------------|
| [**CloseHandle**](icertstore-closehandle.md) | Chiude un handle HCERTSTORE acquisito tramite la proprietà [**storeHandle**](icertstore-storehandle.md) .<br/> |



 

### <a name="properties"></a>Proprietà

L'interfaccia **ICertStore** ha queste proprietà.



| Proprietà                                                     | Tipo di accesso           | Descrizione                                                                                                         |
|:-------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------|
| [**StoreHandle**](icertstore-storehandle.md)<br/>     | Lettura/Scrittura<br/> | Imposta o recupera l'handle HCERTSTORE di un archivio certificati.<br/>                                          |
| [**StoreLocation**](icertstore-storelocation.md)<br/> | Lettura/Scrittura<br/> | Imposta o Recupera il [**\_ \_ percorso dell'archivio CAPICOM**](capicom-store-location.md) di un archivio certificati.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 




