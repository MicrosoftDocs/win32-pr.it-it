---
description: Richiama l'operazione chkdsk sul disco.
ms.assetid: 65942702-b660-46cd-b614-e3e1ec3df7b9
ms.tgt_platform: multiple
title: Metodo Chkdsk della classe Win32_LogicalDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalDisk.Chkdsk
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 24d7052cd7d36da8a9464cbbef142904a70f83767872dadf25fda2033fa66fa6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118959110"
---
# <a name="chkdsk-method-of-the-win32_logicaldisk-class"></a>Metodo Chkdsk della classe LogicalDisk Win32 \_

Il **metodo di istanza chkdsk** richiama l'operazione **chkdsk** sul disco.

Questo argomento usa Managed Object Format (MOF). Per altre informazioni sull'uso di questo metodo, vedere [Chiamata di un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 Chkdsk(
  [in] boolean FixErrors = ,
  [in] boolean VigorousIndexCheck = ,
  [in] boolean SkipFolderCycle = ,
  [in] boolean ForceDismount = ,
  [in] boolean RecoverBadSectors = ,
  [in] boolean OKToRunAtBootUp = 
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*FixErrors* \[ Pollici\]
</dt> <dd>

Indica l'operazione da eseguire per gli errori rilevati sul disco. Se **true,** gli errori vengono corretti. Il valore predefinito è **false**.

</dd> <dt>

*Controllo DisindiceSoluzione* \[ Pollici\]
</dt> <dd>

Se **true,** deve essere eseguito un controllo meno aggressivo delle voci di indice. Il valore predefinito è **false**.

</dd> <dt>

*SkipFolderCycle* \[ Pollici\]
</dt> <dd>

Se **true,** il controllo del ciclo di cartelle deve essere ignorato. Il valore predefinito è **True**.

</dd> <dt>

*ForceDismount* \[ Pollici\]
</dt> <dd>

Se **true,** l'unità deve essere smontata prima del controllo. Il valore predefinito è **false**.

</dd> <dt>

*RecoverBadSectors* \[ Pollici\]
</dt> <dd>

Se **true,** i settori non consentiti devono essere individuati e le informazioni leggibili devono essere recuperate da questi settori. Il valore predefinito è **false**.

</dd> <dt>

*OKToRunAtBootUp* \[ Pollici\]
</dt> <dd>

Se **true,** **l'operazione chkdsk** deve essere eseguita al successivo avvio, nel caso in cui non sia possibile eseguire l'operazione perché il disco è bloccato al momento della chiamata a questo metodo. Il valore predefinito è **false**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il valore 0 (zero) in caso di esito positivo. Altri valori sono elencati nell'elenco seguente. Per altri codici di errore, vedere [**Costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Per i valori **HRESULT** generali, vedere [Codici di errore di sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Operazione riuscita - Chkdsk completato**
</dt> <dd>

0

Operazione riuscita - [**Chkdsk**](chkdsk-method-in-class-win32-logicaldisk.md) completato

</dd> <dt>

**Operazione riuscita - Bloccato e chkdsk pianificato al riavvio**
</dt> <dd>

1

</dd> <dt>

**Errore - File system**
</dt> <dd>

2

</dd> <dt>

**Errore - Errore sconosciuto**
</dt> <dd>

3

</dd> <dt>

**Errore - File system non supportato**
</dt> <dd>

4

</dd> </dl>

## <a name="remarks"></a>Commenti

Questo metodo è applicabile solo alle istanze del disco logico che rappresentano un disco fisico nel computer. Non è applicabile alle unità logiche mappate.

## <a name="examples"></a>Esempio

L'esempio di codice Is[CHKDSK Dirty Bit Set on a server](https://Gallery.TechNet.Microsoft.Com/57076851-97fb-4af6-8c5c-1e34156ceab4) PowerShell esamina il sistema remoto e restituisce true o false se è stato impostato il flag chkdsk /f.

[L'esempio di codice](https://Gallery.TechNet.Microsoft.Com/Remotely-scan-disk-dd4fc267) PowerShell per l'analisi remota del disco avvia o pianifica l'analisi del disco.

L'esempio di codice VBScript seguente viene ChkDsk.exe'unità D in un computer.


```VB
Const FIX_ERRORS = True 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set objDisk = objWMIService.Get("Win32_LogicalDisk.DeviceID='D:'") 
 
errReturn = objDisk.ChkDsk(FIX_ERRORS) 
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Disco logico Win32 \_**](win32-logicaldisk.md)
</dt> <dt>

[Classi hardware del sistema informatico](computer-system-hardware-classes.md)
</dt> </dl>

 

