---
description: Elimina un nome di condivisione dall'elenco di risorse condivise di un server, disconnettendo le connessioni alla risorsa condivisa.
ms.assetid: 175f9c0e-0017-4a86-8e05-ad78e2c93c11
ms.tgt_platform: multiple
title: Metodo Delete della classe Win32_Share
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Share.Delete
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c1331ce9dfa3309c1cfbd0ba0ddc3b4a0c96d431d524d8f0e74f7937c8cdb332
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119918471"
---
# <a name="delete-method-of-the-win32_share-class"></a>Metodo Delete della classe Win32 \_ Share

Il **metodo Elimina** [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) elimina un nome di condivisione dall'elenco di risorse condivise di un server, disconnettendo le connessioni alla risorsa condivisa.

Questo argomento usa Managed Object Format (MOF). Per altre informazioni sull'uso di questo metodo, vedere [Chiamata di un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 Delete();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori elencati nell'elenco seguente o qualsiasi altro valore per indicare un errore. Per altri codici di errore, vedere [**Costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Per i valori **HRESULT** generali, vedere [Codici di errore di sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Operazione** riuscita (0)
</dt> <dt>

**Accesso negato** (2)
</dt> <dt>

**Errore sconosciuto** (8)
</dt> <dt>

**Nome non valido** (9)
</dt> <dt>

**Livello non valido** (10)
</dt> <dt>

**Parametro non** valido (21)
</dt> <dt>

**Condivisione duplicata** (22)
</dt> <dt>

**Percorso reindirizzato** (23)
</dt> <dt>

**Dispositivo o directory sconosciuto** (24)
</dt> <dt>

**Nome di rete non trovato** (25)
</dt> <dt>

**Altro** (26 4294967295)
</dt> </dl>

## <a name="remarks"></a>Commenti

Il **metodo Delete** è un metodo oggetto e viene usato in un'istanza di una classe.

Solo i membri del gruppo locale Administrators o Account Operators o quelli con appartenenza al gruppo operatore Communication, Print o Server possono eseguire correttamente il metodo . L'operatore Print può eliminare solo le code della stampante. L'operatore Communication può eliminare solo le code dei dispositivi di comunicazione.

## <a name="examples"></a>Esempio

L'esempio di codice VBScript seguente elimina la condivisione specificata.


```VB
On Error Resume Next

ComputerName = InputBox("Enter the computer name:", "Delete Share", "localhost")

SName = InputBox("Enter the name of the share:", "Delete Share")



Set Shares = GetObject("winmgmts:\\" & ComputerName & _
 "\root\cimv2").ExecQuery("SELECT * FROM Win32_Share WHERE name = '" & SName & "'")



For Each Share in Shares
 Share.Delete()
Next
```



L'esempio di codice di PowerShell seguente elimina le condivisioni vuote.


```PowerShell
$Shares = Get-WMIObject Win32_Share | Where {$_.Name -eq ""}

Foreach ($Share in $Shares) {
   $Share.Delete()
}
"{0} blank shares found and removed" -f $shares.count
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

[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Condivisione \_ Win32**](win32-share.md)
</dt> </dl>

 

