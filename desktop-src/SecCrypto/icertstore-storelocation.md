---
description: Imposta o Recupera il \_ percorso dell'archivio CAPICOM \_ di un archivio certificati.
ms.assetid: 2bb76f51-f092-4dbe-93e9-1fdc185c7c50
title: 'Proprietà ICertStore:: StoreLocation'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertStore.StoreLocation
- ICertStore.get_StoreLocation
- ICertStore.put_StoreLocation
- CertStore.StoreLocation
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 97bca7ed9dae20c129d202910b40f7c26d54a576
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328600"
---
# <a name="icertstorestorelocation-property"></a>Proprietà ICertStore:: StoreLocation

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.\]

La proprietà **StoreLocation** imposta o Recupera il [**\_ \_ percorso dell'archivio CAPICOM**](capicom-store-location.md) di un archivio certificati.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
CertStore.StoreLocation As CAPICOM_STORE_LOCATION
```



## <a name="property-value"></a>Valore proprietà

Percorso dell'archivio certificati.

## <a name="error-codes"></a>Codici di errore

Se i metodi di accesso alle proprietà **inseriscono \_ StoreLocation** e **get \_ StoreLocation** ha esito positivo, restituiscono S \_ OK.

Qualsiasi altro valore **HRESULT** indica che la chiamata non è riuscita.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ICertStore**](icertstore.md)
</dt> </dl>

 

 




