---
description: Il metodo getlocked recupera lo stato di modifica dell'oggetto (bloccato o sbloccato).
ms.assetid: ecd258db-36bf-41b6-9bdf-537efcf0a46a
title: 'Metodo IAMTimelineObj:: getlocked (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetLocked
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 472b7dedbdbd879d4fa49fe874fb9178d0ccdee4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331274"
---
# <a name="iamtimelineobjgetlocked-method"></a>Metodo IAMTimelineObj:: getlocked

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `GetLocked` metodo recupera lo stato di modifica dell'oggetto (bloccato o sbloccato). Uno stato bloccato indica che l'oggetto non deve essere modificato. uno stato sbloccato indica che l'oggetto può essere modificato. La sequenza temporale non impone il blocco. L'impostazione bloccata esiste solo per praticità dell'applicazione.

## <a name="syntax"></a>Sintassi


```C++
 GetLocked(
   BOOL *pVal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pVal* 
</dt> <dd>

Riceve lo stato di modifica dell'oggetto. Se il valore è **true**, l'oggetto è bloccato e non deve essere modificato. Se **false**, l'oggetto è sbloccato e può essere modificato.

</dd> </dl>

## <a name="remarks"></a>Commenti

> [!Note]  
> Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IAMTimelineObj**](iamtimelineobj.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




