---
description: Comprime il file di voce o la directory della directory logica specificata nel percorso dell'oggetto.
ms.assetid: 4db13622-75c5-45db-8536-451059c0e477
ms.tgt_platform: multiple
title: Metodo Compress della classe Win32_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.Compress
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: ea694c09e11e5801016a4ea85b9774448c542991
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126117"
---
# <a name="compress-method-of-the-win32_directory-class"></a>Metodo Compress della classe di \_ directory Win32

Il metodo **Comprimi** [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) comprime il file di voce o la directory della directory logica specificata nel percorso dell'oggetto.

In questo argomento viene utilizzata la sintassi Managed Object Format (MOF). Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 Compress();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un valore pari a 0 (zero) se il file è stato compresso correttamente e qualsiasi altro numero per indicare un errore.

<dl> <dt>

**0**
</dt> <dd>

La richiesta è stata completata.

</dd> <dt>

**2**
</dt> <dd>

Accesso negato.

</dd> <dt>

**8**
</dt> <dd>

Si è verificato un errore non specificato.

</dd> <dt>

**9**
</dt> <dd>

Il nome specificato non è valido.

</dd> <dt>

**10**
</dt> <dd>

L'oggetto specificato esiste già.

</dd> <dt>

**11**
</dt> <dd>

Il file system non è un NTFS.

</dd> <dt>

**12**
</dt> <dd>

La piattaforma non è Windows.

</dd> <dt>

**13**
</dt> <dd>

L'unità non è la stessa.

</dd> <dt>

**14**
</dt> <dd>

La directory non è vuota.

</dd> <dt>

**15**
</dt> <dd>

Si è verificata una violazione di condivisione.

</dd> <dt>

**16**
</dt> <dd>

Il file di avvio specificato non è valido.

</dd> <dt>

**17**
</dt> <dd>

Un privilegio necessario per l'operazione non viene mantenuto.

</dd> <dt>

**21**
</dt> <dd>

Un parametro specificato non è valido.

</dd> </dl>

## <a name="remarks"></a>Commenti

La compressione consente di liberare spazio di archiviazione aggiuntivo su un'unità disco senza acquistare nuovo hardware e senza rimuovere file o cartelle. A seconda delle dimensioni del disco rigido e del tipo di file archiviati sul disco, è possibile che si riesca a recuperare centinaia di megabyte di spazio su disco, evitando così di dover acquistare un nuovo disco rigido e portare il computer offline fino a quando non viene installata la nuova unità.

Il metodo Compress comprime tutti i file e le sottocartelle all'interno di una cartella specificata. Inoltre, la classe include anche un metodo uncompress che rimuove la compressione da tutti i file e le sottocartelle in una cartella. Vengono inoltre forniti metodi simili con la \_ classe CIM DataFile. In questo modo è possibile comprimere o decomprimere selettivamente file specifici all'interno di una cartella.

Poiché la compressione comporta una lieve riduzione delle prestazioni, non è consigliabile per i file o le cartelle a cui viene eseguito l'accesso in base a una routine. ad esempio, è probabile che non si desideri comprimere i file di database, i file di log o le cartelle dei profili utente. I candidati migliori per la compressione sono file e cartelle a cui non si accede molto spesso. Ad esempio, è possibile scrivere uno script per restituire una raccolta di cartelle in un'unità a cui non è stato eseguito l'accesso per un mese o più, quindi comprimere ognuna di queste cartelle.

La quantità di spazio su disco liberata dalle cartelle di compressione varia a seconda del tipo di file archiviati in tale cartella. Ad esempio, i file con estensione jpg sono già compressi e l'ulteriore compressione ha un effetto minimo sulle dimensioni del file. Con altri tipi di file, tuttavia, il risparmio può essere considerevole. Ad esempio, una nuova cartella è stata creata in un computer di test basato su Windows 2000 e 33 i documenti di Microsoft Word, che occupano un totale di 15 megabyte (MB) di spazio su disco, sono stati copiati in tale cartella. Quando i documenti sono stati compressi, la cartella ha occupato solo 7 MB di spazio su disco.

## <a name="examples"></a>Esempio

L'esempio VBScript seguente comprime la cartella C: \\ Scripts.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colFolders = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_Directory WHERE Name = 'c:\\Scripts'")
For Each objFolder in colFolders
 errResults = objFolder.Compress
 Wscript.Echo errResults
Next
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

[**\_Directory Win32**](win32-directory.md)
</dt> <dt>

[**Decomprimere**](uncompress-method-in-class-win32-directory.md)
</dt> </dl>

 

