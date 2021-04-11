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
ms.openlocfilehash: 2048ba9dac91b139888f27c037d64849de8a4ee8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126922"
---
# <a name="delete-method-of-the-win32_share-class"></a>Metodo Delete della \_ classe Share Win32

Il metodo **Delete** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) Elimina un nome di condivisione dall'elenco di risorse condivise di un server, disconnettendo le connessioni alla risorsa condivisa.

In questo argomento viene utilizzata la sintassi Managed Object Format (MOF). Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 Delete();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori elencati nell'elenco seguente o qualsiasi altro valore per indicare un errore. Per ulteriori codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Operazione riuscita** (0)
</dt> <dt>

**Accesso negato** (2)
</dt> <dt>

**Errore sconosciuto** (8)
</dt> <dt>

**Nome non valido** (9)
</dt> <dt>

**Livello non valido** (10)
</dt> <dt>

**Parametro non valido** (21)
</dt> <dt>

**Condivisione duplicata** (22)
</dt> <dt>

**Percorso reindirizzato** (23)
</dt> <dt>

**Dispositivo o directory sconosciuta** (24)
</dt> <dt>

**Nome NET non trovato** (25)
</dt> <dt>

**Altro** (26 4294967295)
</dt> </dl>

## <a name="remarks"></a>Commenti

Il metodo **Delete** è un metodo oggetto e viene utilizzato in un'istanza di una classe.

Per eseguire correttamente il metodo, solo i membri del gruppo locale Administrators o account Operators o quelli con appartenenza a gruppi di operatori di comunicazione, stampa o server possono eseguire correttamente il metodo. L'operatore Print può eliminare solo le code di stampa. L'operatore di comunicazione può eliminare solo le code del dispositivo di comunicazione.

## <a name="examples"></a>Esempio

Nell'esempio di codice VBScript seguente viene eliminata la condivisione specificata.


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



L'esempio di codice PowerShell seguente elimina le condivisioni vuote.


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
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**\_Condivisione Win32**](win32-share.md)
</dt> </dl>

 

