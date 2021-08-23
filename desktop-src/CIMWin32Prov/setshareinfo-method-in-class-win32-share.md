---
description: SetShareInfo&\# 8194; Il metodo della classe WMI imposta i parametri di una risorsa condivisa.
ms.assetid: f6379261-9325-4b7f-92df-438c5029569f
ms.tgt_platform: multiple
title: Metodo SetShareInfo della Win32_Share classe
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
ms.openlocfilehash: fb9ee76a0b8336ccdca90a04ee3c2a223b7269a30a00276418d6c46a8bb3abc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119800901"
---
# <a name="setshareinfo-method-of-the-win32_share-class"></a>Metodo SetShareInfo della classe Win32 \_ Share

Il metodo della classe [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetShareInfo** imposta i parametri di una risorsa condivisa.

In questo argomento viene Managed Object Format sintassi MOF (Managed Object Format). Per altre informazioni sull'uso di questo metodo, vedere [Chiamata di un metodo](/windows/desktop/WmiSdk/calling-a-method).

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

Limite al numero massimo di utenti autorizzati a usare questa risorsa contemporaneamente.

Esempio: 10. Questo parametro è facoltativo.

</dd> <dt>

*Descrizione* \[ in, facoltativo\]
</dt> <dd>

Commento facoltativo per descrivere la risorsa condivisa.

</dd> <dt>

*Accesso* \[ in, facoltativo\]
</dt> <dd>

Descrittore di sicurezza per le autorizzazioni a livello di utente. Un descrittore di sicurezza contiene informazioni sulle funzionalità di autorizzazione, proprietario e accesso della risorsa. Per altre informazioni, vedere [**Win32 \_ SecurityDescriptor.**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori elencati nell'elenco seguente o qualsiasi altro valore per indicare un errore.

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

**Il metodo SetShareInfo** è un metodo oggetto dinamico e viene usato in un'occorrenza di questa classe.

Solo i membri del gruppo locale Administrators o Account Operators o quelli con appartenenza al gruppo operatore Communication, Print o Server possono eseguire **correttamente SetShareInfo**. L'operatore print può impostare solo code di stampa. L'operatore Communication può impostare solo le code dei dispositivi di comunicazione.

## <a name="examples"></a>Esempio

L'esempio di PowerShell seguente aggiorna il nome della **condivisione newShare.**


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
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Condivisione \_ Win32**](win32-share.md)
</dt> </dl>

 

