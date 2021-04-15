---
title: Classe MSAD_DomainController
description: Rappresenta il controller di dominio in cui è in esecuzione il provider WMI.
ms.assetid: a7671967-79d7-48f8-8869-dd65272e2ed2
ms.tgt_platform: multiple
keywords:
- Classe MSAD_DomainController Active Directory
- Classe MSAD_DomainController Active Directory, descritta
topic_type:
- apiref
api_name:
- MSAD_DomainController
- MSAD_DomainController.DistinguishedName
- MSAD_DomainController.CommonName
- MSAD_DomainController.SiteName
- MSAD_DomainController.NTDsaGUID
- MSAD_DomainController.IsGC
- MSAD_DomainController.TimeOfOldestReplSync
- MSAD_DomainController.TimeOfOldestReplAdd
- MSAD_DomainController.TimeOfOldestReplDel
- MSAD_DomainController.TimeOfOldestReplMod
- MSAD_DomainController.TimeOfOldestReplUpdRefs
- MSAD_DomainController.IsNextRIDPoolAvailable
- MSAD_DomainController.PercentOfRIDsLeft
- MSAD_DomainController.IsRegisteredInDNS
- MSAD_DomainController.IsAdvertisingToLocator
- MSAD_DomainController.IsSysVolReady
api_location:
- replprov.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 303071d3d268953687bc387709c74531f8b40584
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476847"
---
# <a name="msad_domaincontroller-class"></a>\_Classe DomainController MSAD

Rappresenta il controller di dominio in cui è in esecuzione il provider WMI.

## <a name="syntax"></a>Sintassi

``` syntax
[dynamic, provider("ReplProv1")]
class  MSAD_DomainController
{
  String   DistinguishedName;
  String   CommonName;
  String   SiteName;
  String   NTDsaGUID;
  boolean  IsGC = FALSE;
  datetime TimeOfOldestReplSync;
  datetime TimeOfOldestReplAdd;
  datetime TimeOfOldestReplDel;
  datetime TimeOfOldestReplMod;
  datetime TimeOfOldestReplUpdRefs;
  boolean  IsNextRIDPoolAvailable = FALSE;
  uint32   PercentOfRIDsLeft;
  boolean  IsRegisteredInDNS;
  boolean  IsAdvertisingToLocator = FALSE;
  boolean  IsSysVolReady = FALSE;
};
```

## <a name="members"></a>Members

La **classe \_ DomainController MSAD** presenta questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe \_ DomainController MSAD** presenta questi metodi.



| Metodo                                                 | Descrizione                                                                              |
|:-------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| [**ExecuteKCC**](executekcc-msad-domaincontroller.md) | Richiama il controllo di coerenza informazioni per verificare la topologia di replica.<br/> |



 

### <a name="properties"></a>Proprietà

La **classe \_ DomainController MSAD** ha queste proprietà.

<dl> <dt>

**CommonName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene il nome comune dell'oggetto server.

</dd> <dt>

**DistinguishedName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Ottiene il percorso X. 500 dell'oggetto [**NTDS-DSA**](/windows/desktop/ADSchema/c-ntdsdsa) .

</dd> <dt>

**IsAdvertisingToLocator**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene il valore che indica se il servizio localizzatore sul controller di dominio è pubblicizzato correttamente. **True** se il servizio Locator sul controller di dominio viene pubblicizzato correttamente. in caso contrario, **false**.

</dd> <dt>

**IsGC**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene il valore che indica se il controller di dominio è un server di catalogo globale. **True** se il controller di dominio è un server di catalogo globale; in caso contrario, **false**.

</dd> <dt>

**IsNextRIDPoolAvailable**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene il valore che indica se il controller di dominio ha ottenuto un altro pool di RID. **True** se il controller di dominio ha ottenuto un altro pool di RID e l'allocazione di RID in questo controller di dominio può continuare anche se il pool corrente di RID è esaurito. in caso contrario, **false**.

</dd> <dt>

**IsRegisteredInDNS**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene il valore che indica se il controller di dominio è registrato correttamente in DNS. **True** se il controller di dominio è registrato correttamente in DNS; in caso contrario, **false**.

</dd> <dt>

**IsSysVolReady**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene il valore che indica se SysVol è stato pubblicato correttamente. **True** se SYSVOL è stato pubblicato correttamente. in caso contrario, **false**.

</dd> <dt>

**NTDsaGUID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene il GUID associato all'oggetto [**NTDS-DSA**](/windows/desktop/ADSchema/c-ntdsdsa) nel contenitore di configurazione. L'oggetto **NTDS-DSA** rappresenta il processo DSA del servizio dominio di Active Directory nel server.

</dd> <dt>

**PercentOfRIDsLeft**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene la percentuale di RID a sinistra nel pool di RID corrente in questo controller di dominio.

</dd> <dt>

**SiteName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene il sito in cui è presente il controller di dominio.

</dd> <dt>

**TimeOfOldestReplAdd**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene il timestamp dell'operazione di aggiunta della replica meno recente che si trova ancora nella coda del controller di dominio.

</dd> <dt>

**TimeOfOldestReplDel**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene il timestamp dell'operazione di eliminazione della replica meno recente che si trova ancora nella coda del controller di dominio.

</dd> <dt>

**TimeOfOldestReplMod**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene il timestamp dell'operazione di modifica della replica meno recente che si trova ancora nella coda del controller di dominio.

</dd> <dt>

**TimeOfOldestReplSync**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene il timestamp dell'operazione di sincronizzazione della replica meno recente che si trova ancora nella coda del controller di dominio.

</dd> <dt>

**TimeOfOldestReplUpdRefs**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene il timestamp dell'operazione di aggiornamento della replica meno recente che si trova ancora nella coda del controller di dominio.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\MicrosoftActiveDirectory radice<br/>                                               |
| MOF<br/>                      | <dl> <dt>Replprov. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Replprov.dll</dt> </dl> |



 

