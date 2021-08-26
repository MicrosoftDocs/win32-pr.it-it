---
description: Simula una versione chiave.
ms.assetid: EAE84BD5-ECEA-44E7-A7AB-CD18299DF2FE
title: Metodo ReleaseKey della classe Msvm_Keyboard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.ReleaseKey
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1038838ad7ab0c483dd23e77a716da3ffd2474f7a9e8b4fb311b4a141c1ababb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119980131"
---
# <a name="releasekey-method-of-the-msvm_keyboard-class"></a>Metodo ReleaseKey della classe Msvm \_ Keyboard

Simula una versione chiave. In caso di esito positivo, la chiave sarà nello stato attivo.

## <a name="syntax"></a>Sintassi


```mof
uint32 ReleaseKey(
  [in] uint32 keyCode
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*keyCode* \[ Pollici\]
</dt> <dd>

Tipo: **uint32**

Codice della chiave virtuale della chiave da rilasciare. Per l'elenco dei codici di chiave virtuale, vedere [**Codici di chiave virtuale.**](../inputdev/virtual-key-codes.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

Un valore restituito pari a zero indica l'esito positivo. Un valore diverso da zero indica un errore di modifica dello stato della chiave.

<dl> <dt>

**Completata senza errori** (0)
</dt> <dt>

**Parametri del metodo verificati - Processo avviato** (4096)
</dt> <dt>

**Non riuscito** (32768)
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

Il metodo **ReleaseKey** esegue il mapping dei riferimenti rispettivamente a **\_ VK MENU** (18), **VK \_ CONTROL** (17) e **VK \_ SHIFT** (16) a **VK \_ LMENU** (164), **VK \_ LCONTROL** (162) e **VK \_ LSHIFT** (160), perché i codici tasto virtuale **VK \_ MENU,** **VK \_ CONTROL** e **VK \_ SHIFT** non rappresentano tasti reali su una tastiera.

L'accesso alla [**classe Tastiera Msvm \_**](msvm-keyboard.md) potrebbe essere limitato dal filtro di Controllo dell'account utente. Per altre informazioni, vedere [Controllo dell'account utente e WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                              |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                    |
| Spazio dei nomi<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Tastiera \_ Msvm**](msvm-keyboard.md)
</dt> <dt>

[**Codici di chiave virtuale**](../inputdev/virtual-key-codes.md)
</dt> </dl>

 

