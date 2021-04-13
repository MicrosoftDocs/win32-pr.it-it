---
title: Metodo Create della classe Win32_Terminal
description: Crea un terminale con le impostazioni predefinite che possono essere personalizzate usando le proprietà e i metodi delle \_ classi Win32 TerminalSetting.
ms.assetid: 64c90695-72d4-42be-a37a-89b54c04a78c
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto crea metodo
- Create Method Servizi Desktop remoto, classe Win32_Terminal
- Classe Win32_Terminal Servizi Desktop remoto, metodo create
topic_type:
- apiref
api_name:
- Win32_Terminal.Create
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4f1edfa22893452f81cf4695a50380842fa5c06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475641"
---
# <a name="create-method-of-the-win32_terminal-class"></a>Metodo Create della \_ classe terminale Win32

Il metodo **create** crea un terminale con le impostazioni predefinite che possono essere personalizzate usando le proprietà e i metodi delle classi [**Win32 \_ TerminalSetting**](win32-terminalsetting.md) . La funzione restituisce zero in caso di esito positivo e un errore in caso di errore.

## <a name="syntax"></a>Sintassi


```mof
uint32 Create(
  [in] string NewTerminalName,
  [in] string Transport,
  [in] string TerminalProtocol
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*NewTerminalName* \[ in\]
</dt> <dd>

Nome del terminale.

</dd> <dt>

*Trasporto* \[ di in\]
</dt> <dd>

Trasporto per il terminale. Si tratta di una proprietà della classe [**Win32 \_ TSGeneralSetting**](win32-tsgeneralsetting.md) .

</dd> <dt>

*TerminalProtocol* \[ in\]
</dt> <dd>

Protocollo per il terminale. Si tratta di una proprietà della classe [**Win32 \_ TSGeneralSetting**](win32-tsgeneralsetting.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI. Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .

## <a name="remarks"></a>Commenti

I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Terminale Win32**](win32-terminal.md)
</dt> </dl>

 

