---
title: Metodo WSMan. GetErrorMessage (WSManDisp. h)
description: Restituisce una stringa formattata che contiene il testo di un numero di errore.
ms.assetid: 5f0a5259-8356-4406-8612-34f4921184f0
ms.tgt_platform: multiple
keywords:
- Gestione remota Windows del Metodo GetErrorMessage
- Metodo GetErrorMessage Gestione remota Windows, oggetto WSMan
- Gestione remota Windows oggetto WSMan, Metodo GetErrorMessage
topic_type:
- apiref
api_name:
- WSMan.GetErrorMessage
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d085e6f19c64f609fe1389a2822df1594ee69bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340693"
---
# <a name="wsmangeterrormessage-method"></a>WSMan. GetErrorMessage, metodo

Restituisce una stringa formattata che contiene il testo di un numero di errore. Questo metodo esegue la stessa operazione del *numero di errore decimale o esadecimale* della riga **di comando WinRM** **helpmsg** .

## <a name="syntax"></a>Sintassi


```VB
WSMan.GetErrorMessage( _
  ByVal errorNumber, _
  ByRef errorMessage _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*numero errore* \[ in\]
</dt> <dd>

Numero del messaggio di errore in formato decimale o esadecimale da WinRM, WinHTTP o altri componenti del sistema operativo.

</dd> <dt>

*ErrorMessage* \[ out\]
</dt> <dd>

Stringa del messaggio di errore formattata come i messaggi restituiti dal comando **WinRM** .

</dd> </dl>

## <a name="remarks"></a>Commenti

Il metodo C++ corrispondente è [**IWSManEx:: GetErrorMessage**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-geterrormessage).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                 |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                           |
| Intestazione<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>WSManDisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**WSMan**](wsman.md)
</dt> </dl>

 

 





