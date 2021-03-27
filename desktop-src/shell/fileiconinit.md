---
description: Inizializza o reinizializza l'elenco di immagini di sistema.
ms.assetid: 4e661326-157e-4c75-86df-cd213e01c3e5
title: FileIconInit (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIconInit
api_type:
- DllExport
api_location:
- Shell32.dll
ms.openlocfilehash: 090f35cc576caf6f99a8d5822a0304f15383e8db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345416"
---
# <a name="fileiconinit-function"></a>FileIconInit (funzione)

Inizializza o reinizializza l'elenco di immagini di sistema.

## <a name="syntax"></a>Sintassi


```C++
BOOL FileIconInit(
  _In_ BOOL fRestoreCache
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*fRestoreCache* \[ in\]
</dt> <dd>

Tipo: **bool**

**True** per ripristinare la cache dell'immagine di sistema dal disco; In caso contrario, **false** .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **bool**

**True** se la cache è stata aggiornata correttamente, **false** se l'inizializzazione non è riuscita.

## <a name="remarks"></a>Commenti

Se si utilizzano elenchi di immagini di sistema nel proprio processo, è necessario chiamare **FileIconInit** negli orari seguenti:

-   All'avvio.
-   In risposta a un messaggio [**WM \_ SETTINGCHANGE**](../winmsg/wm-settingchange.md) quando viene impostato il flag [**SPI \_ SETNONCLIENTMETRICS**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) .

**FileIconInit** non è incluso in un file di intestazione. È necessario chiamarlo direttamente da Shell32.dll, usando il numero ordinale 660.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                            |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 
