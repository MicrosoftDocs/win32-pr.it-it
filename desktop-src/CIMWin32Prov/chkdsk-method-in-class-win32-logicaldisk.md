---
description: Richiama l'operazione Chkdsk sul disco.
ms.assetid: 65942702-b660-46cd-b614-e3e1ec3df7b9
ms.tgt_platform: multiple
title: Metodo CHKDSK della classe Win32_LogicalDisk
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
ms.openlocfilehash: 662fc8739f90eea15295b762edc446ac16677aef
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127223"
---
# <a name="chkdsk-method-of-the-win32_logicaldisk-class"></a>Metodo CHKDSK della classe Win32 \_ disco logico

Il metodo dell'istanza **chkdsk** richiama l'operazione **chkdsk** sul disco.

In questo argomento viene utilizzata la sintassi Managed Object Format (MOF). Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).

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

*FixErrors* \[ in\]
</dt> <dd>

Indica cosa fare per gli errori rilevati nel disco. Se **true**, gli errori sono corretti. Il valore predefinito è **false**.

</dd> <dt>

*VigorousIndexCheck* \[ in\]
</dt> <dd>

Se **true**, deve essere eseguita una verifica meno vigorosa delle voci di indice. Il valore predefinito è **false**.

</dd> <dt>

*SkipFolderCycle* \[ in\]
</dt> <dd>

Se **true**, il controllo del ciclo di cartelle deve essere ignorato. Il valore predefinito è **True**.

</dd> <dt>

*ForceDismount* \[ in\]
</dt> <dd>

Se **true**, l'unità deve essere disinstallata prima del controllo. Il valore predefinito è **false**.

</dd> <dt>

*RecoverBadSectors* \[ in\]
</dt> <dd>

Se **true**, i settori danneggiati devono essere individuati e le informazioni leggibili devono essere recuperate da questi settori. Il valore predefinito è **false**.

</dd> <dt>

*OKToRunAtBootUp* \[ in\]
</dt> <dd>

Se **true**, l'operazione **chkdsk** deve essere eseguita al momento dell'avvio successivo, nel caso in cui non sia stato possibile eseguire l'operazione perché il disco è bloccato al momento della chiamata di questo metodo. Il valore predefinito è **false**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore pari a 0 (zero) se ha esito positivo. Gli altri valori sono elencati nell'elenco seguente. Per ulteriori codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Operazione riuscita-Chkdsk completata**
</dt> <dd>

0

Operazione riuscita- [**chkdsk**](chkdsk-method-in-class-win32-logicaldisk.md) completata

</dd> <dt>

**Operazione riuscita-bloccato e CHKDSK pianificati al riavvio**
</dt> <dd>

1

</dd> <dt>

**Errore-file system sconosciuto**
</dt> <dd>

2

</dd> <dt>

**Errore-errore sconosciuto**
</dt> <dd>

3

</dd> <dt>

**Errore-file System non supportato**
</dt> <dd>

4

</dd> </dl>

## <a name="remarks"></a>Commenti

Questo metodo è applicabile solo alle istanze del disco logico che rappresentano un disco fisico nel computer. Non è applicabile alle unità logiche mappate.

## <a name="examples"></a>Esempio

Il[valore del bit dirty CHKDSK impostato in un](https://Gallery.TechNet.Microsoft.Com/57076851-97fb-4af6-8c5c-1e34156ceab4) esempio di codice PowerShell del server esamina il sistema remoto e restituisce true o false se è stato impostato il flag chkdsk/f.

L'esempio di codice PowerShell per l' [analisi remota del disco](https://Gallery.TechNet.Microsoft.Com/Remotely-scan-disk-dd4fc267) avvia in modalità remota o Pianifica il disco di analisi.

Nell'esempio di codice VBScript seguente viene eseguito ChkDsk.exe sull'unità D in un computer.


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
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Disco logico Win32**](win32-logicaldisk.md)
</dt> <dt>

[Classi hardware del sistema del computer](computer-system-hardware-classes.md)
</dt> </dl>

 

