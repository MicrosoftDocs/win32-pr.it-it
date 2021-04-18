---
title: Interfaccia IVMKeyboard (VPCCOMInterfaces. h)
description: Controlla il dispositivo della tastiera all'interno di una macchina virtuale. Il IVMKeyboard di una macchina virtuale può essere recuperato usando la proprietà della tastiera IVMVirtualMachine.
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
ms.openlocfilehash: fce2ddddd00de509278760a22fe3ab464f27c1c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302560"
---
# <a name="ivmkeyboard-interface"></a>Interfaccia IVMKeyboard

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Controlla il dispositivo della tastiera all'interno di una macchina virtuale. Il **IVMKeyboard** di una macchina virtuale può essere recuperato usando la proprietà [**IVMVirtualMachine:: Keyboard**](ivmvirtualmachine-keyboard.md) .

## <a name="members"></a>Membri

L'interfaccia **IVMKeyboard** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMKeyboard** dispone anche di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'interfaccia **IVMKeyboard** dispone di questi metodi.



| Metodo                                                       | Descrizione                                                                   |
|:-------------------------------------------------------------|:------------------------------------------------------------------------------|
| [**IsPressed**](ivmkeyboard-ispressed.md)                   | Determina se il tasto specificato è inattivo.<br/>                      |
| [**PressAndReleaseKey**](ivmkeyboard-pressandreleasekey.md) | Simula un tasto premuto e quindi rilasciato.<br/>              |
| [**PressKey**](ivmkeyboard-presskey.md)                     | Simula un tasto premuto.<br/>                                |
| [**ReleaseKey**](ivmkeyboard-releasekey.md)                 | Simula una chiave rilasciata.<br/>                                    |
| [**TypeAsciiText**](ivmkeyboard-typeasciitext.md)           | Simula una serie di chiavi ASCII digitate nel guest.<br/>       |
| [**TypeKeySequence**](ivmkeyboard-typekeysequence.md)       | Simula un elenco delimitato da virgole di chiavi digitate nel guest.<br/> |



 

### <a name="properties"></a>Proprietà

L'interfaccia **IVMKeyboard** ha queste proprietà.



| Proprietà                                                                | Tipo di accesso           | Descrizione                                                                                                |
|:------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------|
| [**HasExclusiveAccess**](ivmkeyboard-hasexclusiveaccess.md)<br/> | Lettura/Scrittura<br/> | Indica se l'oggetto dispone del controllo esclusivo sul dispositivo della tastiera della macchina virtuale.<br/> |



 

## <a name="remarks"></a>Commenti

Le chiavi possono essere digitate nella macchina virtuale in diversi modi. Per digitare una normale sequenza ASCII di caratteri, usare il metodo [**TypeAsciiText**](ivmkeyboard-typeasciitext.md) . Se è necessaria una maggiore flessibilità, **IVMKeyboard** dispone di diversi metodi progettati per essere utilizzati con i codici chiave elencati di seguito. Il metodo [**TypeKeySequence**](ivmkeyboard-typekeysequence.md) può accettare una stringa delimitata da virgole di codici chiave, che verrà premuta e rilasciata nell'ordine, all'interno della macchina virtuale. Oltre a questi codici chiave, è possibile usare le parole chiave su e giù per forzare la pressione di una chiave solo o rilasciarla. Le parole chiave UP e DOWN si applicano solo al codice chiave che segue direttamente la parola chiave.

Per evitare che più script, applicazioni o utenti tentino simultaneamente di accedere allo stesso dispositivo della tastiera, impostare la proprietà [**HasExclusiveAccess**](ivmkeyboard-hasexclusiveaccess.md) su **true**. Se l'accesso esclusivo viene acquisito da un processo, eventuali tentativi da parte di altri processi di inviare input al dispositivo della tastiera verranno ignorati fino a quando non viene rilasciato l'accesso esclusivo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMKeyboard è definito come 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4<br/>                |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce Virtual PC Windows](virtual-pc-interfaces.md)
</dt> <dt>

[Sequenze di chiavi](key-sequences.md)
</dt> </dl>

 

