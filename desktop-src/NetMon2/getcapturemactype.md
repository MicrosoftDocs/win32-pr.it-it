---
description: La funzione GetCaptureMacType restituisce il tipo MAC di una determinata acquisizione.
ms.assetid: de0dfb36-df3a-4f6e-b266-09c81dfdc88b
title: Funzione GetCaptureMacType (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCaptureMacType
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 73569109db5b958e854135461a0e480178d0105a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750095"
---
# <a name="getcapturemactype-function"></a>GetCaptureMacType (funzione)

La funzione **GetCaptureMacType** restituisce il tipo Mac di una determinata acquisizione.

## <a name="syntax"></a>Sintassi


```C++
DWORD WINAPI GetCaptureMacType(
  _In_ HCAPTURE hCapture
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hCapture* \[ in\]
</dt> <dd>

Handle per l'acquisizione. Per informazioni sull'acquisizione dell'handle di acquisizione, vedere la sezione Osservazioni in questo argomento **GetCaptureMacType** .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è uno dei tipi MAC seguenti.

-   \_tipo Mac \_ sconosciuto
-   \_Ethernet di tipo Mac \_
-   \_Tokenring di tipo Mac \_
-   \_FDDI di tipo Mac \_

Se la funzione ha esito negativo, il valore restituito è un codice di errore.



| Codice restituito                                                                                              | Descrizione                                                 |
|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>**\_tipo Mac \_ NMERR \_ sconosciuto**</dt> </dl> | Network Monitor non è riuscito a trovare un tipo MAC noto.<br/> |



 

## <a name="remarks"></a>Commenti

L'handle dell'acquisizione può essere ottenuto in diversi modi, a seconda dell'utente che effettua la chiamata. Per gli esperti, l'handle viene specificato nel membro **hCapture** della struttura [EXPERTSTARTUPINFO](expertstartupinfo.md) . Per i parser, è possibile ottenere l'handle di acquisizione chiamando la funzione [GetFrameCaptureHandle](getframecapturehandle.md) .

Gli [*esperti*](e.md) e i [*parser*](p.md) possono chiamare la funzione **GetCaptureMacType** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmap. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




