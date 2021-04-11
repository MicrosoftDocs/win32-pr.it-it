---
description: SetShareInfo&\# 8194; Il metodo della classe WMI imposta i parametri di una risorsa condivisa.
ms.assetid: f6379261-9325-4b7f-92df-438c5029569f
ms.tgt_platform: multiple
title: Metodo SetShareInfo della classe Win32_Share
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Share.SetShareInfo
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 54b599ed3124c0d06468bd15589d6aa8a93fb7c1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225789"
---
# <a name="setshareinfo-method-of-the-win32_share-class"></a>Metodo SetShareInfo della classe di \_ condivisione Win32

Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetShareInfo** imposta i parametri di una risorsa condivisa.

In questo argomento viene utilizzata la sintassi Managed Object Format (MOF). Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 SetShareInfo(
  [in, optional] uint32                   MaximumAllowed,
  [in, optional] string                   Description,
  [in, optional] Win32_SecurityDescriptor Access
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*MaximumAllowed* \[ in, facoltativo\]
</dt> <dd>

Limite per il numero massimo di utenti che possono usare questa risorsa contemporaneamente.

Esempio: 10. Questo parametro è facoltativo.

</dd> <dt>

*Descrizione* \[ di in, facoltativo\]
</dt> <dd>

Commento facoltativo per descrivere la risorsa condivisa.

</dd> <dt>

*Accesso* \[ a in, facoltativo\]
</dt> <dd>

Descrittore di sicurezza per le autorizzazioni a livello di utente. Un descrittore di sicurezza contiene informazioni sulle funzionalità di autorizzazione, proprietario e accesso della risorsa. Per ulteriori informazioni, vedere [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori elencati nell'elenco seguente o qualsiasi altro valore per indicare un errore.

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

Il metodo **SetShareInfo** è un metodo di oggetto dinamico e viene usato su un'occorrenza di questa classe.

Solo i membri del gruppo locale Administrators o account Operators o quelli con appartenenza a gruppi di operatori di comunicazione, stampa o server possono eseguire correttamente **SetShareInfo**. L'operatore Print può impostare solo le code della stampante. L'operatore di comunicazione può impostare solo le code del dispositivo di comunicazione.

## <a name="examples"></a>Esempio

L'esempio di PowerShell seguente aggiorna il nome della condivisione **newShare** .


```PowerShell
$newShare = Get-WmiObject win32_share | Where-Object {$_.name -eq "newShare"}
[void]$newShare.SetShareInfo($null,"This is my new description",$null)
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

 

