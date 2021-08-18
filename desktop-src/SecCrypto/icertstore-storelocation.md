---
description: Imposta o recupera l'archivio CAPICOM \_ LOCATION di un archivio \_ certificati.
ms.assetid: 2bb76f51-f092-4dbe-93e9-1fdc185c7c50
title: Proprietà ICertStore::StoreLocation
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
ms.openlocfilehash: ea11da4fc908a2a3b665b2491614dbffeaa3034a3127617c562c3365522df835
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005609"
---
# <a name="icertstorestorelocation-property"></a>Proprietà ICertStore::StoreLocation

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.\]

La **proprietà StoreLocation** imposta o recupera [**capiCOM STORE \_ \_ LOCATION**](capicom-store-location.md) di un archivio certificati.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
CertStore.StoreLocation As CAPICOM_STORE_LOCATION
```



## <a name="property-value"></a>Valore proprietà

Percorso dell'archivio certificati.

## <a name="error-codes"></a>Codici di errore

Se i metodi di accesso alle **proprietà \_ put StoreLocation** e **get \_ StoreLocation** hanno esito positivo, restituiscono S \_ OK.

Qualsiasi altro **valore HRESULT** indica che la chiamata non è riuscita.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ICertStore**](icertstore.md)
</dt> </dl>

 

 




