---
title: Metodo IVMVirtualPC CreateVirtualMachine (VPCCOMInterfaces. h)
description: Crea una nuova configurazione di macchina virtuale e recupera l'oggetto macchina virtuale.
ms.assetid: 35f7364f-debd-4b9c-8240-23c0512eb004
keywords:
- Metodo CreateVirtualMachine Virtual PC
- Metodo CreateVirtualMachine Virtual PC, interfaccia IVMVirtualPC
- Interfaccia IVMVirtualPC Virtual PC, metodo CreateVirtualMachine
topic_type:
- apiref
api_name:
- IVMVirtualPC.CreateVirtualMachine
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 494d5166271e6c4086b8dfee12deb61e32ae8a18
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478154"
---
# <a name="ivmvirtualpccreatevirtualmachine-method"></a>Metodo IVMVirtualPC:: CreateVirtualMachine

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Crea una nuova configurazione di macchina virtuale e recupera l'oggetto macchina virtuale.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CreateVirtualMachine(
  [in]          BSTR              configurationName,
  [in]          BSTR              configurationPath,
  [out, retval] IVMVirtualMachine **virtualMachine
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ConfigurationName* \[ in\]
</dt> <dd>

Nome della macchina virtuale da creare. La lunghezza del nome non può superare i 80 caratteri e la lunghezza combinata del nome e del percorso dei file VMC e VMCX non può superare il numero massimo di caratteri di **\_ percorso** (260). Quando vengono creati i file di configurazione, il nome file Extensions. vmc e. vmcx verrà aggiunto alla fine del nome della macchina virtuale. Se questo parametro è **null** o una stringa vuota, il parametro *configurationPath* deve specificare il percorso completo del file vmc.

</dd> <dt>

*configurationPath* \[ in\]
</dt> <dd>

Percorso della cartella che conterrà il file VMC. Questa cartella verrà creata se non esiste. Se *ConfigurationName* è **null** o una stringa vuota, è necessario specificare il percorso completo del nuovo file di configurazione.

</dd> <dt>

*virtualmachine* \[ out, retval\]
</dt> <dd>

Puntatore a un nuovo oggetto [**IVMVirtualMachine**](ivmvirtualmachine.md) che rappresenta la macchina virtuale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                                            | Descrizione                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                  | L'operazione è stata completata.<br/>                                                                                                                                                                       |
| <dl> <dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt> </dl>                                    | Il parametro *ConfigurationName* o *configurationPath* non è valido oppure il parametro *virtualmachine* è **null**.<br/>                                                                               |
| <dl> <dt>**HRESULT \_ DA \_ Win32 ( \_ percorso errore \_ non \_ trovato)**</dt> <dt>0 x 80070003</dt> </dl> | Il sistema non è in grado di trovare il percorso specificato dal parametro *configurationPath* .<br/>                                                                                                                     |
| <dl> <dt>**HRESULT \_ DA \_ Win32 (errore \_ nome non valido \_ )**</dt> <dt>0x8007007b</dt> </dl>    | Il parametro *configurationPath* contiene un carattere non valido (uno di " \* ?: <>/ \| " ").<br/>                                                                                                        |
| <dl> <dt>**HRESULT \_ DA \_ Win32 (errore \_ \_ percorso errato)**</dt> <dt>0x800700a1</dt> </dl>    | Il parametro *configurationPath* specifica un percorso vuoto o relativo. È necessario specificare un percorso assoluto.<br/>                                                                                                |
| <dl> <dt>**HRESULT \_ Da \_ Win32 (overflow del buffer degli errori \_ \_ )**</dt> <dt>0x8007006f</dt> </dl> | Il percorso specificato dai parametri *ConfigurationName* e *configurationPath* restituisce un percorso troppo lungo. La lunghezza totale del percorso deve essere minore di **Max \_ path** (260) caratteri.<br/> |
| <dl> <dt>**HRESULT \_ DA \_ Win32 (errore \_ già \_ esistente)**</dt> <dt>0x800700b7</dt> </dl>  | Un file di configurazione con questo nome esiste già in questa posizione.<br/>                                                                                                                                |
| <dl> <dt>**Macchina virtuale \_ E \_ config \_ senza \_ nome**</dt> <dt>0xA0040400</dt> </dl>                       | Il parametro *ConfigurationName* è vuoto.<br/>                                                                                                                                                         |
| <dl> <dt>**Macchina virtuale \_ Nome di configurazione di E \_ \_ \_ troppo \_ lungo**</dt> <dt>0xA0040401</dt> </dl>                | Il parametro *ConfigurationName* è di lunghezza superiore a 80 caratteri.<br/>                                                                                                                                  |
| <dl> <dt>**Macchina virtuale \_ Il \_ nome di configurazione E 0xA0040402 \_ non è \_ valido \_**</dt> <dt></dt> </dl>            | Il parametro *ConfigurationName* contiene un carattere non valido (uno di " \* ?: <>/ \| \\ " ").<br/>                                                                                                      |
| <dl> <dt>**Macchina virtuale \_ E \_ config \_ \_ nome duplicato**</dt> <dt>0xA0040403</dt> </dl>                | Esiste già una macchina virtuale con questo nome.<br/>                                                                                                                                                  |
| <dl> <dt>**Macchina virtuale \_ E \_ \_ virtualizzazione hardware \_ disabilitato**</dt> <dt>0xA0040951</dt> </dl>     | Il processore non supporta le estensioni di virtualizzazione accelerata hardware (HAV).<br/>                                                                                                                |
| <dl> <dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt> </dl>                            | Si è verificato un errore imprevisto.<br/>                                                                                                                                                                   |



 

## <a name="remarks"></a>Commenti

I nomi delle macchine virtuali non fanno distinzione tra maiuscole e minuscole, ad esempio, "MyVM" e "MyVM" si riferiscono alla stessa macchina virtuale.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualPC è definito come 236ba0d9-A24A-4292-A132-27c1421dfd01<br/>               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

