---
description: "Metodo GetAccessMask della classe Win32_Share: restituisce una bitmap uint32 con i diritti di accesso alla condivisione mantenuta dall'utente o dal gruppo per conto del quale viene restituita l'istanza."
ms.assetid: 234f44a4-ffff-431d-a973-98f2bd313c7d
ms.tgt_platform: multiple
title: Metodo GetAccessMask della classe Win32_Share
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Share.GetAccessMask
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: ebc2b2620b0bdc019e117f9a4b2c376be6320be968fdae42509dc3f62c3cc9a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077661"
---
# <a name="getaccessmask-method-of-the-win32_share-class"></a>Metodo GetAccessMask della classe Win32 \_ Share

Il **metodo GetAccessMask** restituisce una bitmap uint32 con i diritti di accesso alla condivisione mantenuta dall'utente o dal gruppo per conto del quale viene restituita l'istanza.

Questo argomento usa Managed Object Format (MOF). Per altre informazioni sull'uso di questo metodo, vedere [Chiamata di un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 GetAccessMask();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Diritti di accesso alla condivisione mantenuta dall'utente o dal gruppo.

<dl> <dt>

**DIRECTORY \_ ELENCO \_ FILE**
</dt> <dd>

1 (0x1)

Concede il diritto di leggere i dati dal file. Per una directory, questo valore concede il diritto di elencare il contenuto della directory.

</dd> <dt>

**FILE \_ AGGIUNGI \_ FILE**
</dt> <dd>

2 (0x2)

Concede il diritto di scrivere dati nel file. Per una directory, questo valore concede il diritto di creare un file nella directory.

</dd> <dt>

**FILE \_ AGGIUNGI \_ SOTTODIRECTORY**
</dt> <dd>

4 (0x4)

Concede il diritto di aggiungere dati al file. Per una directory, questo valore concede il diritto di creare una sottodirectory.

</dd> <dt>

**FILE \_ READ \_ EA**
</dt> <dd>

8 (0x8)

Concede il diritto di leggere gli attributi estesi.

</dd> <dt>

**FILE \_ WRITE \_ EA**
</dt> <dd>

16 (0x10)

Concede il diritto di scrivere attributi estesi.

</dd> <dt>

**ATTRAVERSAMENTO \_ FILE**
</dt> <dd>

32 (0x20)

Concede il diritto di eseguire un file. Per una directory, la directory può essere attraversata.

</dd> <dt>

**FILE \_ DELETE \_ CHILD**
</dt> <dd>

64 (0x40)

Concede il diritto di eliminare una directory e tutti i file che contiene (i relativi elementi figlio), anche se i file sono di sola lettura.

</dd> <dt>

**ATTRIBUTI \_ DI LETTURA \_ FILE**
</dt> <dd>

128 (0x80)

Concede il diritto di leggere gli attributi del file.

</dd> <dt>

**ATTRIBUTI \_ DI SCRITTURA \_ FILE**
</dt> <dd>

256 (0x100)

Concede il diritto di modificare gli attributi del file.

</dd> <dt>

**DELETE**
</dt> <dd>

65536 (0x10000)

Concede l'accesso per l'eliminazione.

</dd> <dt>

**CONTROLLO \_ LETTURA**
</dt> <dd>

131072 (0x20000)

Concede l'accesso in lettura al descrittore di sicurezza e al proprietario.

</dd> <dt>

**APPLICAZIONE \_ LIVELLO DATI WRITE**
</dt> <dd>

262144 (0x40000)

Concede l'accesso in scrittura all'elenco di controllo di accesso discrezionale (DACL).

</dd> <dt>

**WRITE \_ OWNER**
</dt> <dd>

524288 (0x80000)

Assegna il proprietario della scrittura.

</dd> <dt>

**Sincronizzare**
</dt> <dd>

1048576 (0x100000)

Sincronizza l'accesso e consente a un processo di attendere che un oggetto entri nello stato segnalato.

</dd> </dl>

## <a name="remarks"></a>Commenti

**Il metodo GetAccessMask** è un metodo oggetto e viene usato in un'occorrenza di questa classe.

## <a name="examples"></a>Esempio

L'esempio di codice VBScript seguente crea una cartella di condivisione e quindi ottiene il valore della maschera di accesso nel descrittore di sicurezza che protegge la cartella di condivisione.


```VB
Const FILE_SHARE = 0
Const MAXIMUM_CONNECTIONS = 4000 
strComputer = "."

Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set objNewShare = objWMIService.Get("Win32_Share")
Return = objNewShare.Create ("C:\Temp", "TestShare", FILE_SHARE, MAXIMUM_CONNECTIONS, "test share")

If Return <> 0 Then
          WScript.Echo Return
          WScript.Quit
End If

Set objShare = objWMIService.Get("Win32_Share.Name='TestShare'")
Return = objShare.GetAccessMask
WScript.Echo Return
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

[**Condivisione \_ Win32**](win32-share.md)
</dt> </dl>

 

