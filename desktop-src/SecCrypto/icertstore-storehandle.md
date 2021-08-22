---
description: Imposta o recupera l'handle HCERTSTORE di un archivio certificati.
ms.assetid: 3ff8b4c7-4a9a-4cc1-b0ea-da442ebce157
title: Proprietà ICertStore::StoreHandle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertStore.StoreHandle
- ICertStore.get_StoreHandle
- ICertStore.put_StoreHandle
- CertStore.StoreHandle
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2858e7484c82663b2ba6866d0f17b5528921619dbfa80cbb76ec0eabbb39a332
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005619"
---
# <a name="icertstorestorehandle-property"></a>Proprietà ICertStore::StoreHandle

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.\]

La **proprietà StoreHandle** imposta o recupera l'handle HCERTSTORE di un archivio certificati.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
CertStore.StoreHandle As Long
```



## <a name="property-value"></a>Valore proprietà

Handle HCERTSTORE dell'archivio certificati.

## <a name="error-codes"></a>Codici di errore

Se i metodi di accesso alle **proprietà \_ put StoreHandle** **e get \_ StoreHandle** hanno esito positivo, restituiscono S \_ OK.

Qualsiasi altro **valore HRESULT** indica che la chiamata non è riuscita.

## <a name="remarks"></a>Commenti

È necessario chiamare il [**metodo CloseHandle**](icertstore-closehandle.md) o la [**funzione CertCloseStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore) per liberare il contesto.

Se si imposta la **proprietà StoreHandle,** lo stato dell'intero [**oggetto Store**](store.md) viene reimpostato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ICertStore**](icertstore.md)
</dt> </dl>

 

 




