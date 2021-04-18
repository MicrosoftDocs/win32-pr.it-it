---
description: È possibile usare il metodo AddAsString dell'oggetto SWbemPrivilegeSet per aggiungere un privilegio a una raccolta SWbemPrivilegeSet usando una stringa di privilegio.
ms.assetid: 729ed4e3-2c5c-4bb4-acc6-cf9ad0d5eaf1
ms.tgt_platform: multiple
title: Metodo SWbemPrivilegeSet. AddAsString (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilegeSet.AddAsString
- ISWbemPrivilegeSet.AddAsString
- ISWbemPrivilegeSet.AddAsString
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: b3a740141b14766080a09d01b36b5c0202351eda
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318502"
---
# <a name="swbemprivilegesetaddasstring-method"></a>SWbemPrivilegeSet. AddAsString, metodo

È possibile usare il metodo **AddAsString** dell'oggetto [**SWbemPrivilegeSet**](swbemprivilegeset.md) per aggiungere un privilegio a una raccolta **SWbemPrivilegeSet** usando una stringa di privilegio. Utilizzare questo metodo per aggiungere un privilegio o per abilitare un privilegio per gli oggetti [**SWbemSecurity**](swbemsecurity.md) . Vedere [esecuzione di operazioni con privilegi tramite VBScript](executing-privileged-operations-using-vbscript.md).

Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintassi


```VB
objPrivilege = .AddAsString( _
  ByVal strPrivilege, _
  [ ByVal bIsEnabled ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*strPrivilege* 
</dt> <dd>

Obbligatorio. Una delle stringhe dei privilegi. Per un elenco completo di queste stringhe e delle costanti WMI associate, vedere [**costanti Privilege**](privilege-constants.md). Ogni stringa di privilegio rappresenta un privilegio specifico. Ad esempio, per aggiungere il privilegio utilizzato da per arrestare un computer, utilizzare la stringa **SeShutdownPrivilege** .

</dd> <dt>

*bIsEnabled* \[ opzionale\]
</dt> <dd>

Valore booleano che Abilita o Disabilita questo privilegio. Il valore predefinito è **True**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se ha esito positivo, questo metodo restituisce un oggetto [**SWbemPrivilege**](swbemprivilege.md) che rappresenta il nuovo privilegio. In caso contrario, viene restituito un oggetto null.

## <a name="error-codes"></a>Codici di errore

Al termine del metodo **AddAsString** , l'oggetto **Err** può contenere il codice di errore riportato nell'elenco seguente.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Errore non specificato.

</dd> </dl>

## <a name="examples"></a>Esempio

L'esempio di codice VBScript seguente crea una nuova porta per un server di stampa usando [**Win32 \_ TCPIPPrinterPort**](/windows/desktop/CIMWin32Prov/win32-tcpipprinterport). Per questa operazione è necessario **SeLoadDriverPrivilege** . Vedere [esecuzione di operazioni con privilegi](executing-privileged-operations.md).


```VB
Set objWMIService = GetObject("Winmgmts:")
objWMIService.Security_.Privileges. _
    AddAsString "SeLoadDriverPrivilege", True
Set objNewPort = objWMIService.Get _
    ("Win32_TCPIPPrinterPort").SpawnInstance_
objNewPort.Name = "IP_111.222.111.11"
objNewPort.Protocol = 1
objNewPort.HostAddress = "111.222.111.11"
objNewPort.PortNumber = "9999"
objNewPort.SNMPEnabled = False
objNewPort.Put_
```



Un esempio di codice che usa questo metodo è descritto anche nell'argomento [**SWbemPrivilegeSet**](swbemprivilegeset.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMPRIVILEGESET CLSID<br/>                                                     |
| IID<br/>                      | \_ISWBEMPRIVILEGESET IID<br/>                                                      |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SWbemPrivilegeSet**](swbemprivilegeset.md)
</dt> <dt>

[**SWbemPrivilegeSet. Add**](swbemprivilegeset-add.md)
</dt> <dt>

[**SWbemPrivilegeSet. Remove**](swbemprivilegeset-remove.md)
</dt> <dt>

[**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dt>

[**Costanti Privilege**](privilege-constants.md)
</dt> <dt>

[Esecuzione di operazioni con privilegi](executing-privileged-operations.md)
</dt> <dt>

[Esecuzione di operazioni con privilegi tramite VBScript](executing-privileged-operations-using-vbscript.md)
</dt> </dl>

 

