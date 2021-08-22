---
title: Metodo IVMVirtualPC RegisterVirtualMachine (VPCCOMInterfaces.h)
description: Registra una configurazione di macchina virtuale esistente e recupera l'oggetto macchina virtuale.
ms.assetid: d3b13f1b-7537-4e3f-9bcc-98a6fe855f78
keywords:
- Metodo RegisterVirtualMachine Virtual PC
- Metodo RegisterVirtualMachine Virtual PC, interfaccia IVMVirtualPC
- Interfaccia IVMVirtualPC Virtual PC, metodo RegisterVirtualMachine
topic_type:
- apiref
api_name:
- IVMVirtualPC.RegisterVirtualMachine
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3752b613bb3adc97d1e0968d989b5c97c616b76883ef89880be7c00d720c62a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998534"
---
# <a name="ivmvirtualpcregistervirtualmachine-method"></a>Metodo IVMVirtualPC::RegisterVirtualMachine

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Registra una configurazione di macchina virtuale esistente e recupera l'oggetto macchina virtuale.

## <a name="syntax"></a>Sintassi


```C++
HRESULT RegisterVirtualMachine(
  [in]          BSTR              configurationName,
  [in]          BSTR              configurationPath,
  [out, retval] IVMVirtualMachine **virtualMachine
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*configurationName* \[ Pollici\]
</dt> <dd>

Nome della macchina virtuale da registrare. La lunghezza del nome non può superare gli 80 caratteri e la lunghezza combinata del nome e del percorso non può superare i 260 caratteri **MAX \_ PATH** (260). Il nome specificato può contenere l'estensione vmc. Se questo parametro è **NULL** o una stringa vuota, il *parametro configurationPath* deve specificare il percorso completo del file di configurazione.

</dd> <dt>

*configurationPath* \[ Pollici\]
</dt> <dd>

Percorso della cartella che contiene il file di configurazione esistente. Se il *parametro configurationName* è **NULL** o una stringa vuota, è necessario specificare il percorso completo del file di configurazione esistente.

</dd> <dt>

*virtualMachine* \[ out, retval\]
</dt> <dd>

Puntatore a un nuovo [**oggetto IVMVirtualMachine**](ivmvirtualmachine.md) che rappresenta questa macchina virtuale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                                            | Descrizione                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                  | L'operazione è stata completata.<br/>                                                                                                                                                                          |
| <dl> <dt>**E \_ Puntatore**</dt> <dt>0x80004003</dt> </dl>                                    | Il *parametro configurationName* *o configurationPath* non è valido oppure *virtualMachine* è **NULL.**<br/>                                                                                                  |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ PATH NOT \_ \_ FOUND) 0X80070003**</dt> <dt></dt> </dl> | Il sistema non riesce a trovare il percorso specificato dai *parametri configurationName* *e configurationPath.*<br/>                                                                                               |
| <dl> <dt>**HRESULT \_ DA \_ WIN32(FILE \_ DI ERRORE NON \_ \_ TROVATO)**</dt> <dt>0X80070002</dt> </dl> | Il sistema non riesce a trovare il file specificato dai *parametri configurationName* *e configurationPath.*<br/>                                                                                               |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ INVALID \_ NAME)**</dt> <dt>0x8007007b</dt> </dl>    | Il *parametro configurationPath* contiene un carattere non valido (uno di " \* ?:<>/ \| "").<br/>                                                                                                           |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ BAD \_ PATHNAME)**</dt> <dt>0x800700a1</dt> </dl>    | Il parametro *configurationPath* parametro specifica un percorso vuoto o relativo. È necessario un percorso assoluto.<br/>                                                                                         |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ BUFFER \_ OVERFLOW)**</dt> <dt>0x8007006f</dt> </dl> | Il percorso specificato dai parametri *configurationName* e *configurationPath* determina un percorso troppo lungo. La lunghezza combinata del percorso deve essere minore di **MAX \_ PATH** (260).<br/> |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ ALREADY \_ EXISTS)**</dt> <dt>0x800700b7</dt> </dl>  | In questo percorso esiste già un file di configurazione con questo nome.<br/>                                                                                                                                   |
| <dl> <dt>**Macchina virtuale \_ E \_ NOME DI CONFIGURAZIONE TROPPO LUNGO \_ \_ \_ 0XA0040401**</dt> <dt></dt> </dl>                | Il *parametro configurationName* supera gli 80 caratteri.<br/>                                                                                                                                     |
| <dl> <dt>**Macchina virtuale \_ E \_ CONFIG NAME INVALID \_ \_ \_ CHAR**</dt> <dt>0xA0040402</dt> </dl>            | Il *parametro configurationName* contiene un carattere non valido (uno di " \* ?:<>/ \| \\ "").<br/>                                                                                                         |
| <dl> <dt>**Macchina virtuale \_ E \_ CONFIG DUPLICATE NAME \_ \_ 0xA0040403**</dt> <dt></dt> </dl>                | Esiste già una macchina virtuale con questo nome.<br/>                                                                                                                                                     |
| <dl> <dt>**Macchina virtuale \_ E \_ \_ VIRTUALIZZAZIONE HARDWARE \_ DISABILITATA**</dt> <dt>0XA0040951</dt> </dl>     | Il processore non supporta le estensioni haV (Hardware Accelerated Virtualization).<br/>                                                                                                                   |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                            | Si è verificato un errore imprevisto.<br/>                                                                                                                                                                      |



 

## <a name="remarks"></a>Commenti

I nomi delle macchine virtuali non fanno distinzione tra maiuscole e minuscole, ad esempio "MyVM" e "myvm" fanno riferimento alla stessa macchina virtuale.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMVirtualPC è definito come \_ 236ba0d9-a24a-4292-a132-27c1421dfd01<br/>               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

