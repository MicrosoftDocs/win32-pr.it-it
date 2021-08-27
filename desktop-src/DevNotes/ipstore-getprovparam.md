---
description: Progettato per impostare le informazioni sui parametri specificati.
ms.assetid: e1a5766f-a303-47f1-a4bb-33f4253a5464
title: Metodo IPStore::GetProvParam (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.GetProvParam
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: de18c4452456ed98f7e5214a33445a0780189f7864d96cfb05e08123a3b42cc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955910"
---
# <a name="ipstoregetprovparam-method"></a>Metodo IPStore::GetProvParam

\[Protected Archiviazione (Pstore) è disponibile per l'uso in Windows Server 2003 e Windows XP. È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive. Pstore usa un'implementazione precedente della protezione dei dati. Gli sviluppatori sono fortemente invitati a sfruttare la protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData.**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)\]

\[Questo metodo non è implementato.\]

Progettato per impostare le informazioni sui parametri specificati. Si noti, tuttavia, che non è implementato e avrà sempre esito negativo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetProvParam(
  [in]  DWORD dwParam,
  [out] DWORD *pcbData,
  [out] BYTE  **ppbData,
  [in]  DWORD dwFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dwParam* \[ Pollici\]
</dt> <dd>

Riservato.

</dd> <dt>

*pcbData* \[ Cambio\]
</dt> <dd>

Riservato.

</dd> <dt>

*ppbData* \[ Cambio\]
</dt> <dd>

Riservato.

</dd> <dt>

*dwFlags* \[ Pollici\]
</dt> <dd>

Riservato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Le chiamate a questo metodo avranno sempre esito negativo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Pstore.h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Archivio IP**](ipstore.md)
</dt> </dl>

 

 
