---
description: Esclude i dischi dall'operazione Autochk da eseguire al riavvio successivo.
ms.assetid: 5df2bc3b-e149-4853-aa02-af4cb8af6da0
ms.tgt_platform: multiple
title: Metodo ExcludeFromAutochk della classe Win32_LogicalDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalDisk.ExcludeFromAutochk
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c41d93111742e975490d97169c7e9147ba5fb1ce
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304692"
---
# <a name="excludefromautochk-method-of-the-win32_logicaldisk-class"></a>Metodo ExcludeFromAutochk della \_ classe disco logico Win32

Il metodo **ExcludeFromAutochk** esclude i dischi dall'operazione **Autochk** da eseguire al riavvio successivo.

In questo argomento viene utilizzata la sintassi Managed Object Format (MOF). Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 ExcludeFromAutochk(
  [in] string LogicalDisk[]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Disco logico* \[ in\]
</dt> <dd>

Elenco di unità che devono essere escluse da **Autochk** al riavvio successivo. La sintassi della stringa è costituita dalla lettera di unità seguita da due punti per il disco logico.

Esempio: "C:"

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore pari a 0 (zero) quando non si verifica alcun errore. I valori sono elencati nell'elenco seguente. Per ulteriori codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Operazione riuscita** (0)
</dt> <dt>

**Errore-unità remota** (1)
</dt> <dt>

**Errore-unità rimovibile** (2)
</dt> <dt>

**Errore-unità non directory radice** (3)
</dt> <dt>

**Errore-unità sconosciuta** (4)
</dt> </dl>

## <a name="remarks"></a>Commenti

Se non viene escluso, **Autochk** viene eseguito sul disco quando è impostato il bit dirty per il disco. Si noti che le chiamate per escludere dischi non sono cumulative. Se viene effettuata una chiamata per escludere alcuni dischi, il nuovo elenco non viene aggiunto all'elenco di dischi già contrassegnati per l'esclusione. Il nuovo elenco di dischi sovrascrive l'elenco precedente. Questo metodo è applicabile solo alle istanze del disco logico che rappresentano un disco fisico nel computer. Non è applicabile alle unità logiche mappate.

## <a name="examples"></a>Esempio

Nell'esempio di codice VBScript seguente si garantisce che Autochk.exe non venga eseguito sull'unità C alla successiva riavvio del computer, anche se l'unità C è stata impostata sul "bit dirty".


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set objDisk = objWMIService.Get("Win32_LogicalDisk") 
 
errReturn = objDisk.ExcludeFromAutoChk(Array("C:")) 
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

 

