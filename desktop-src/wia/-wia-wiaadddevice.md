---
description: La funzione WiaAddDevice richiama l'interfaccia utente dell'installazione guidata dello scanner e della fotocamera. Equivale a eseguire &\# 0034; rundll32.exe sti \_ci.dll AddDevice&\# 0034; dal prompt dei comandi.
ms.assetid: 83a1e22c-d751-4c8e-8f39-ec987042c745
title: Funzione WiaAddDevice (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WiaAddDevice
api_type:
- LibDef
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 694265f0a59096a5a6a58ccbf4e43c92e21fe9b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751751"
---
# <a name="wiaadddevice-function"></a>WiaAddDevice (funzione)

La funzione **WiaAddDevice** richiama l'interfaccia utente dell'installazione guidata dello scanner e della fotocamera. È equivalente all'esecuzione di "rundll32.exe STI \_ci.dll AddDevice" dal prompt dei comandi.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI WiaAddDevice(void);
```



## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Questa funzione deve essere chiamata con le credenziali di amministratore. Quando si esegue il controllo dell'account utente (LUA), il processo deve essere elevato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                         |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>WIA. h</dt> </dl>       |
| Libreria<br/>                  | <dl> <dt>Wiaguid. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**InstallWiaDevice**](-wia-installwiadevice.md)
</dt> </dl>

 

 




