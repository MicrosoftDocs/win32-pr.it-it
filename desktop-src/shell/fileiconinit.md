---
description: Inizializza o reinizializza l'elenco di immagini di sistema.
ms.assetid: 4e661326-157e-4c75-86df-cd213e01c3e5
title: Funzione FileIconInit
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
ms.openlocfilehash: 1771e1f0bde83f0fc7d070787b7a19f87007e26bd1ad42dcaa88e230e61a60af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111811"
---
# <a name="fileiconinit-function"></a>Funzione FileIconInit

Inizializza o reinizializza l'elenco di immagini di sistema.

## <a name="syntax"></a>Sintassi


```C++
BOOL FileIconInit(
  _In_ BOOL fRestoreCache
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*fRestoreCache* \[ Pollici\]
</dt> <dd>

Tipo: **BOOL**

**TRUE per** ripristinare la cache delle immagini di sistema dal disco. **FALSE in** caso contrario.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **BOOL**

**TRUE** se la cache è stata aggiornata correttamente, **FALSE se** l'inizializzazione non è riuscita.

## <a name="remarks"></a>Commenti

Se si usano elenchi di immagini di sistema nel proprio processo, è necessario chiamare **FileIconInit** nei momenti seguenti:

-   All'avvio.
-   In risposta a un [**messaggio WM \_ SETTINGCHANGE**](../winmsg/wm-settingchange.md) quando è impostato il flag [**SPI \_ SETNONCLIENTMETRICS.**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)

**FileIconInit** non è incluso in un file di intestazione. È necessario chiamarlo direttamente da Shell32.dll, usando l'ordinale 660.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                            |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 
