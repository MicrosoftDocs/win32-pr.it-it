---
description: Recupera lo stato della chiave di una chiave.
ms.assetid: 4AEB732D-274E-42BB-AA97-9E4D30B81338
title: Metodo IsKeyPressed della classe Msvm_Keyboard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.IsKeyPressed
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: bb8b4e2da0a6f1cd3c30e3d65404ecf308c71e88483e322193497216586b20b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118392444"
---
# <a name="iskeypressed-method-of-the-msvm_keyboard-class"></a>Metodo IsKeyPressed della classe Keyboard \_ msvm

Recupera lo stato della chiave di una chiave.

## <a name="syntax"></a>Sintassi


```mof
uint32 IsKeyPressed(
  [in]  uint32  keyCode,
  [out] boolean keyState
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*keyCode* \[ Pollici\]
</dt> <dd>

Tipo: **uint32**

Codice della chiave virtuale della chiave su cui eseguire la query. Per l'elenco dei codici di chiave virtuale, vedere [**Codici di chiave virtuale**](../inputdev/virtual-key-codes.md).

</dd> <dt>

*keyState* \[ Cambio\]
</dt> <dd>

Tipo: **booleano**

Stato di in giù corrente della chiave. Un **valore True** indica che la chiave non è disponibile.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

Un valore restituito pari a zero indica l'esito positivo. Un valore diverso da zero indica un errore durante la query sullo stato della chiave.

<dl> <dt>

**Completato senza errori** (0)
</dt> <dt>

**Parametri del metodo controllati - Processo avviato** (4096)
</dt> <dt>

**Operazione non** riuscita (32768)
</dt> <dt>

**Accesso negato** (32769)
</dt> <dt>

**Non supportato** (32770)
</dt> <dt>

**Lo stato è sconosciuto** (32771)
</dt> <dt>

**Timeout** (32772)
</dt> <dt>

**Parametro non** valido (32773)
</dt> <dt>

**Sistema in uso** (32774)
</dt> <dt>

**Stato non valido per questa operazione** (32775)
</dt> <dt>

**Tipo di dati non** corretto (32776)
</dt> <dt>

**Il sistema non è disponibile** (32777)
</dt> <dt>

**Memoria insufficiente** (32778)
</dt> </dl>

## <a name="remarks"></a>Commenti

Il metodo **IsKeyPressed** restituirà sempre **False** per **VK \_ MENU** (18), **VK \_ CONTROL** (17) e **VK \_ SHIFT** (16) perché non si tratta di tasti reali su una tastiera. Questi codici chiave virtuale vengono sempre mappati rispettivamente a **VK \_ LMENU** (164), **VK \_ LCONTROL** (162) e **VK \_ LSHIFT** (160), rispettivamente, dai [**metodi PressKey**](presskey-msvm-keyboard.md) [**e ReleaseKey.**](releasekey-msvm-keyboard.md)

L'accesso alla [**classe Tastiera Msvm \_**](msvm-keyboard.md) potrebbe essere limitato dal filtro del controllo dell'account utente. Per altre informazioni, vedere [Controllo dell'account utente e WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                              |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                    |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Tastiera \_ Msvm**](msvm-keyboard.md)
</dt> <dt>

[**Codici di chiave virtuale**](../inputdev/virtual-key-codes.md)
</dt> </dl>

 

