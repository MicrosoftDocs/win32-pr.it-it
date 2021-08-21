---
description: Posiziona il servizio rappresentato dall'oggetto PrinterDriver Win32 \_ nello stato arrestato.
ms.assetid: 0e730fe6-ff9f-4866-a255-be6d372f2d7d
ms.tgt_platform: multiple
title: Metodo StopService della Win32_PrinterDriver classe (Sdoias.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterDriver.StopService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0ec49d6f5b9c7efcb860ba99eaf7984fa89cfb0bc12cbdfcfe8bde0db95eff1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119020399"
---
# <a name="stopservice-method-of-the-win32_printerdriver-class"></a>Metodo StopService della classe PrinterDriver Win32 \_

Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **StopService** posiziona il servizio rappresentato dall'oggetto [**\_ PrinterDriver Win32**](win32-printerdriver.md) nello stato arrestato.

Questo argomento usa Managed Object Format (MOF). Per altre informazioni sull'uso di questo metodo, vedere [Chiamata di un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 StopService();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori elencati nell'elenco seguente o qualsiasi altro valore per indicare un errore. Per valori diversi da quelli elencati nell'elenco seguente, vedere [**Costanti di errore WMI.**](/windows/desktop/WmiSdk/wmi-error-constants)

<dl> <dt>

**0**
</dt> <dd>

Il servizio è stato arrestato correttamente.

</dd> <dt>

**1**
</dt> <dd>

Richiesta non supportata.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                      |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                        |
| Intestazione<br/>                   | <dl> <dt>Sdoias.h</dt> </dl>           |
| MOF<br/>                      | <dl> <dt>Win32 \_ Printer.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Classi hardware del sistema computer](computer-system-hardware-classes.md)
</dt> <dt>

[**Win32 \_ PrinterDriver**](win32-printerdriver.md)
</dt> </dl>

 

