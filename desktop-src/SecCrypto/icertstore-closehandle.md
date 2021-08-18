---
description: Chiude un handle HCERTSTORE acquisito tramite la proprietà StoreHandle.
ms.assetid: 1b0d3d9b-09e0-4035-88ac-2887b3ab60c9
title: Metodo ICertStore::CloseHandle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertStore.CloseHandle
- CertStore.CloseHandle
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3d6f1b0b44cd0fdc71f8f3d37fa9bd8290c5d606eea1f97f5bf6644f9ce8e2a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005659"
---
# <a name="icertstoreclosehandle-method"></a>Metodo ICertStore::CloseHandle

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.\]

Il **metodo CloseHandle** chiude un handle HCERTSTORE acquisito tramite la [**proprietà StoreHandle.**](icertstore-storehandle.md)

## <a name="syntax"></a>Sintassi


```VB
CertStore.CloseHandle( _
  ByVal hCertStore _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hCertStore* \[ Pollici\]
</dt> <dd>

Handle HCERTSTORE da chiudere.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è **HRESULT.** Il valore **S \_ OK indica** l'esito positivo. Qualsiasi altro valore indica che l'operazione non è riuscita.

## <a name="remarks"></a>Commenti

Questo metodo non rilascia l'handle HCERTSTORE contenuto in un [**oggetto**](store.md) Store. Deve essere usato solo per rilasciare un handle HCERTSTORE acquisito tramite la [**proprietà StoreHandle.**](icertstore-storehandle.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ICertStore**](icertstore.md)
</dt> </dl>

 

 




