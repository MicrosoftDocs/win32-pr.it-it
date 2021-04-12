---
description: Recupera lo stato della chiave di una chiave.
ms.assetid: 4AEB732D-274E-42BB-AA97-9E4D30B81338
title: Metodo KeyPressed della classe Msvm_Keyboard
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
ms.openlocfilehash: 44af7a3dc82c0d4d20a2e4c6aff21f7a47837490
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226625"
---
# <a name="iskeypressed-method-of-the-msvm_keyboard-class"></a>Metodo KeyPressed della \_ classe della tastiera MSVM

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

*codice* \[ di stato in\]
</dt> <dd>

Tipo: **UInt32**

Codice della chiave virtuale della chiave su cui eseguire la query. Per l'elenco dei codici delle chiavi virtuali, vedere [**codici a chiave virtuale**](../inputdev/virtual-key-codes.md).

</dd> <dt>

*stato* \[ della pagina out\]
</dt> <dd>

Tipo: **booleano**

Stato di inattività corrente della chiave. Un valore **true** indica che la chiave è inattiva.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **UInt32**

Un valore restituito pari a zero indica esito positivo. Un valore diverso da zero indica un errore di query sullo stato della chiave.

<dl> <dt>

**Completato senza errori** (0)
</dt> <dt>

**Parametri del metodo controllati-processo avviato** (4096)
</dt> <dt>

**Non riuscito** (32768)
</dt> <dt>

**Accesso negato** (32769)
</dt> <dt>

**Non supportato** (32770)
</dt> <dt>

**Stato sconosciuto** (32771)
</dt> <dt>

**Timeout** (32772)
</dt> <dt>

**Parametro non valido** (32773)
</dt> <dt>

**Sistema in uso** (32774)
</dt> <dt>

**Stato non valido per l'operazione** (32775)
</dt> <dt>

**Tipo di dati non corretto** (32776)
</dt> <dt>

**Sistema non disponibile** (32777)
</dt> <dt>

**Memoria insufficiente** (32778)
</dt> </dl>

## <a name="remarks"></a>Commenti

Il metodo **keypressed** restituirà sempre **false** per il **\_ menu VK** (18), il **\_ controllo VK** (17) e lo **\_ spostamento VK** (16) perché non si tratta di chiavi reali su una tastiera. A questi codici delle chiavi virtuali viene sempre eseguito il mapping a **VK \_ LMENU** (164), **VK \_ LCONTROL** (162) e **VK \_ LSHIFT** (160) rispettivamente dai metodi [**pulsanteper**](presskey-msvm-keyboard.md) e [**ReleaseKey**](releasekey-msvm-keyboard.md) .

L'accesso alla classe della [**\_ tastiera MSVM**](msvm-keyboard.md) potrebbe essere limitato dal filtraggio del controllo dell'account utente. Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                                    |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Tastiera MSVM**](msvm-keyboard.md)
</dt> <dt>

[**Codici chiave virtuale**](../inputdev/virtual-key-codes.md)
</dt> </dl>

 

