---
description: Restituisce informazioni sul provider di archiviazione.
ms.assetid: bdacb5bb-a37a-4970-add7-57625bec1ce0
title: 'Metodo IPStore:: GetInfo (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.GetInfo
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 7747c3acf15a60f5556a8855ef4825715ef5050b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324280"
---
# <a name="ipstoregetinfo-method"></a>Metodo IPStore:: GetInfo

\[L'archiviazione protetta (PStore) è disponibile per l'uso in Windows Server 2003 e Windows XP. È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive. PStore usa un'implementazione precedente della protezione dei dati. Gli sviluppatori sono vivamente invitati a sfruttare i vantaggi della protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Restituisce informazioni sul provider di archiviazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetInfo(
  [out] PPST_PROVIDERINFO *ppProperties
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppProperties* \[ out\]
</dt> <dd>

Puntatore a una struttura **PPST \_ ProviderInfo restituito da** che contiene informazioni sul provider di archiviazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è un valore **HRESULT** . Il valore **pst \_ E \_ OK** indica che la funzione ha avuto esito positivo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PStore. h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IPStore**](ipstore.md)
</dt> </dl>

 

 
