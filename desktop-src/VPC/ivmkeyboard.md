---
title: Interfaccia IVMKeyboard (VPCCOMInterfaces.h)
description: Controlla il dispositivo tastiera all'interno di una macchina virtuale. L'IVMKeyboard per una macchina virtuale può essere recuperata usando la proprietà IVMVirtualMachine Keyboard.
ms.assetid: a64a23b6-3937-40c6-af9d-fb341c04fbf7
keywords:
- Interfaccia IVMKeyboard Virtual PC
- Interfaccia IVMKeyboard Virtual PC, descritta
topic_type:
- apiref
api_name:
- IVMKeyboard
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7284c4e2bb164cd53c8a34357c881ed096f342ae2c2230422985fac4c1fdae9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118344798"
---
# <a name="ivmkeyboard-interface"></a>Interfaccia IVMKeyboard

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Controlla il dispositivo tastiera all'interno di una macchina virtuale. **L'IVMKeyboard** per una macchina virtuale può essere recuperata usando la [**proprietà IVMVirtualMachine::Keyboard.**](ivmvirtualmachine-keyboard.md)

## <a name="members"></a>Membri

**L'interfaccia IVMKeyboard** eredita dall'interfaccia [**IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IVMKeyboard** include anche questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

**L'interfaccia IVMKeyboard** include questi metodi.



| Metodo                                                       | Descrizione                                                                   |
|:-------------------------------------------------------------|:------------------------------------------------------------------------------|
| [**Ispressed**](ivmkeyboard-ispressed.md)                   | Determina se la chiave specificata è in giù.<br/>                      |
| [**PressAndReleaseKey**](ivmkeyboard-pressandreleasekey.md) | Simula la pressione e il rilascio di un tasto.<br/>              |
| [**PressKey**](ivmkeyboard-presskey.md)                     | Simula la pressione di un tasto.<br/>                                |
| [**ReleaseKey**](ivmkeyboard-releasekey.md)                 | Simula il rilascio di un tasto.<br/>                                    |
| [**TypeAsciiText**](ivmkeyboard-typeasciitext.md)           | Simula una serie di chiavi ASCII digitate nel guest.<br/>       |
| [**TypeKeySequence**](ivmkeyboard-typekeysequence.md)       | Simula un elenco delimitato da virgole di chiavi digitate nel guest.<br/> |



 

### <a name="properties"></a>Proprietà

**L'interfaccia IVMKeyboard** ha queste proprietà.



| Proprietà                                                                | Tipo di accesso           | Descrizione                                                                                                |
|:------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------|
| [**HasExclusiveAccess**](ivmkeyboard-hasexclusiveaccess.md)<br/> | Lettura/Scrittura<br/> | Indica se questo oggetto ha il controllo esclusivo sul dispositivo tastiera della macchina virtuale.<br/> |



 

## <a name="remarks"></a>Commenti

Le chiavi possono essere digitate nella macchina virtuale in diversi modi. Per digitare una normale sequenza di caratteri ASCII, usare il [**metodo TypeAsciiText.**](ivmkeyboard-typeasciitext.md) Se è necessaria una maggiore flessibilità, **IVMKeyboard** dispone di diversi metodi progettati per essere usati con i codici chiave nell'elenco seguente. Il [**metodo TypeKeySequence**](ivmkeyboard-typekeysequence.md) può accettare una stringa delimitata da virgole di codici chiave, che verranno premuti e rilasciati, in ordine, all'interno della macchina virtuale. Oltre a questi codici chiave, le parole chiave UP e DOWN possono essere usate per forzare la pressione o il rilascio di un solo tasto. Le parole chiave UP e DOWN si applicano solo al codice della chiave che segue direttamente la parola chiave .

Per evitare che più script, applicazioni o utenti tentino contemporaneamente di accedere allo stesso dispositivo tastiera, impostare la proprietà [**HasExclusiveAccess**](ivmkeyboard-hasexclusiveaccess.md) su **TRUE.** Se un processo acquisisce l'accesso esclusivo, qualsiasi tentativo da parte di altri processi di inviare input al dispositivo da tastiera verrà ignorato finché non viene rilasciato l'accesso esclusivo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMKeyboard è definito come 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4<br/>                |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Windows Interfacce di Virtual PC](virtual-pc-interfaces.md)
</dt> <dt>

[Sequenze di chiavi](key-sequences.md)
</dt> </dl>

 

