---
description: Restituisce un puntatore al commento di un'acquisizione.
ms.assetid: 3ef5c5b3-5586-469f-8975-049713715403
title: Funzione GetCaptureComment (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCaptureComment
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: ca2d3dd3fdc91c54c49b12119a56180396df5ec5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305917"
---
# <a name="getcapturecomment-function"></a>GetCaptureComment (funzione)

La funzione **GetCaptureComment** restituisce un puntatore al commento di un'acquisizione.

## <a name="syntax"></a>Sintassi


```C++
LPSTR WINAPI GetCaptureComment(
  _In_ HCAPTURE hCapture
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hCapture* \[ in\]
</dt> <dd>

Handle per l'acquisizione. Per ulteriori informazioni su come ottenere l'handle di acquisizione, vedere la sezione Osservazioni.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, ovvero se l'acquisizione contiene un commento, il valore restituito è un puntatore alla stringa di commento.

Se la funzione ha esito negativo, il valore restituito è **null**.

## <a name="remarks"></a>Commenti

Non modificare la stringa di commento restituita che corrisponde alla stringa di commento effettiva presente nell'acquisizione caricata. Qualsiasi modifica può danneggiare l'acquisizione. Il tentativo di modificare la stringa genera una violazione di accesso.

L'handle dell'acquisizione può essere ottenuto in diversi modi, a seconda se la chiamata viene eseguita da un esperto o da un parser. Per gli esperti, l'handle viene specificato nel membro **hCapture** della struttura [EXPERTSTARTUPINFO](expertstartupinfo.md) . Per i parser, è possibile ottenere l'handle di acquisizione chiamando la funzione [GetFrameCaptureHandle](getframecapturehandle.md) .

Per recuperare il commento di un'acquisizione dal relativo file di acquisizione, chiamare la funzione [GetCaptureCommentFromFilename](getcapturecommentfromfilename.md) .

Gli [*esperti*](e.md) e i [*parser*](p.md) possono chiamare la funzione **GetCaptureComment** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmap. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[EXPERTSTARTUPINFO](expertstartupinfo.md)
</dt> <dt>

[GetCaptureCommentFromFilename](getcapturecommentfromfilename.md)
</dt> <dt>

[GetFrameCaptureHandle](getframecapturehandle.md)
</dt> </dl>

 

 




