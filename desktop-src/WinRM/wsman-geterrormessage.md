---
title: Metodo WSMan.GetErrorMessage (WSManDisp.h)
description: Restituisce una stringa formattata che contiene il testo di un numero di errore.
ms.assetid: 5f0a5259-8356-4406-8612-34f4921184f0
ms.tgt_platform: multiple
keywords:
- Metodo GetErrorMessage Windows gestione remota
- Metodo GetErrorMessage Windows gestione remota , oggetto WSMan
- Oggetto WSMan Windows gestione remota, metodo GetErrorMessage
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
ms.openlocfilehash: 94e7f23a5d2678d3df024c78397aaeb6a388d8b75368f329867f6457b9ad4d84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742091"
---
# <a name="wsmangeterrormessage-method"></a>Metodo WSMan.GetErrorMessage

Restituisce una stringa formattata che contiene il testo di un numero di errore. Questo metodo esegue la stessa operazione della riga di comando **Winrm winrm** **helpmsg** decimale o numero di errore *esadecimale*.

## <a name="syntax"></a>Sintassi


```VB
WSMan.GetErrorMessage( _
  ByVal errorNumber, _
  ByRef errorMessage _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*errorNumber* \[ Pollici\]
</dt> <dd>

Numero di messaggio di errore in formato decimale o esadecimale da WinRM, WinHTTP o altri componenti del sistema operativo.

</dd> <dt>

*errorMessage* \[ Cambio\]
</dt> <dd>

Stringa di messaggio di errore formattata come messaggi restituiti dal **comando Winrm.**

</dd> </dl>

## <a name="remarks"></a>Commenti

Il metodo C++ corrispondente è [**IWSManEx::GetErrorMessage**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-geterrormessage).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                 |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                           |
| Intestazione<br/>                   | <dl> <dt>WSManDisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>WSManDisp.idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>WSManDisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**WSMan**](wsman.md)
</dt> </dl>

 

 





