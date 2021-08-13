---
description: Esclude i dischi dall'operazione autochk da eseguire al riavvio successivo.
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
ms.openlocfilehash: a37171c594cb3a51b131220bb604234bcae108fa025ea6343da99fdc998a7dc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118676129"
---
# <a name="excludefromautochk-method-of-the-win32_logicaldisk-class"></a>Metodo ExcludeFromAutochk della classe LogicalDisk Win32 \_

Il **metodo ExcludeFromAutochk** esclude i dischi dall'operazione **autochk** da eseguire al riavvio successivo.

Questo argomento usa Managed Object Format (MOF). Per altre informazioni sull'uso di questo metodo, vedere [Chiamata di un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 ExcludeFromAutochk(
  [in] string LogicalDisk[]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Disco logico* \[ Pollici\]
</dt> <dd>

Elenco di unità che devono essere escluse da **autochk** al riavvio successivo. La sintassi della stringa è costituita dalla lettera di unità seguita da due punti per il disco logico.

Esempio: "C:"

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il valore 0 (zero) quando non si verifica alcun errore. I valori sono elencati nell'elenco seguente. Per altri codici di errore, [**vedere Costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum.**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum) Per i valori **HRESULT** generali, vedere [Codici di errore di sistema.](/windows/desktop/Debug/system-error-codes)

<dl> <dt>

**Operazione** riuscita (0)
</dt> <dt>

**Errore - Unità remota** (1)
</dt> <dt>

**Errore - Unità rimovibile** (2)
</dt> <dt>

**Errore - Unità non directory radice** (3)
</dt> <dt>

**Errore - Unità sconosciuta** (4)
</dt> </dl>

## <a name="remarks"></a>Commenti

Se non è escluso, **autochk** viene eseguito sul disco quando la dirty bit è impostata per il disco. Si noti che le chiamate per escludere i dischi non sono cumulative. Se viene effettuata una chiamata per escludere alcuni dischi, il nuovo elenco non viene aggiunto all'elenco di dischi già contrassegnati per l'esclusione. Il nuovo elenco di dischi sovrascrive l'elenco precedente. Questo metodo è applicabile solo alle istanze del disco logico che rappresentano un disco fisico nel computer. Non è applicabile alle unità logiche mappate.

## <a name="examples"></a>Esempio

L'esempio di codice VBScript seguente garantisce che il Autochk.exe non verrà eseguito sull'unità C al successivo riavvio del computer, anche se "dirty bit" è stato impostato sull'unità C.


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
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Disco logico \_ Win32**](win32-logicaldisk.md)
</dt> <dt>

[Classi hardware del sistema computer](computer-system-hardware-classes.md)
</dt> </dl>

 

