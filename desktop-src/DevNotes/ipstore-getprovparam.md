---
description: Progettato per impostare le informazioni sui parametri specificati.
ms.assetid: e1a5766f-a303-47f1-a4bb-33f4253a5464
title: 'Metodo IPStore:: GetProvParam (PStore. h)'
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
ms.openlocfilehash: ac45c08f64658d176449d76456e737a1a37dc2b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324801"
---
# <a name="ipstoregetprovparam-method"></a>Metodo IPStore:: GetProvParam

\[L'archiviazione protetta (PStore) è disponibile per l'uso in Windows Server 2003 e Windows XP. È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive. PStore usa un'implementazione precedente della protezione dei dati. Gli sviluppatori sono vivamente invitati a sfruttare i vantaggi della protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

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

*dwParam* \[ in\]
</dt> <dd>

Riservato.

</dd> <dt>

*pcbData* \[ out\]
</dt> <dd>

Riservato.

</dd> <dt>

*ppbData* \[ out\]
</dt> <dd>

Riservato.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Riservato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Le chiamate a questo metodo avranno sempre esito negativo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PStore. h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IPStore**](ipstore.md)
</dt> </dl>

 

 
