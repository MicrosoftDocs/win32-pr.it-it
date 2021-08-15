---
title: MSAD_DomainController classe
description: Rappresenta il controller di dominio in cui è in esecuzione il provider WMI.
ms.assetid: a7671967-79d7-48f8-8869-dd65272e2ed2
ms.tgt_platform: multiple
keywords:
- MSAD_DomainController class Active Directory
- MSAD_DomainController classe Active Directory , descritta
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
ms.openlocfilehash: a428d1c852d93fb34bfc3188219bd8ffdc5020ae65c5f9191c44d075b603a143
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118186086"
---
# <a name="msad_domaincontroller-class"></a>Classe \_ DomainController MSAD

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

La **classe \_ MsAD DomainController** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe \_ MsAD DomainController** include questi metodi.



| Metodo                                                 | Descrizione                                                                              |
|:-------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| [**ExecuteKCC**](executekcc-msad-domaincontroller.md) | Richiama il controllo di coerenza delle informazioni per verificare la topologia di replica.<br/> |



 

### <a name="properties"></a>Proprietà

La **classe MSAD \_ DomainController** ha queste proprietà.

<dl> <dt>

**CommonName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene il nome comune dell'oggetto server.

</dd> <dt>

**Distinguishedname**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Ottiene il percorso X.500 [**dell'oggetto NTDS-DSA.**](/windows/desktop/ADSchema/c-ntdsdsa)

</dd> <dt>

**IsAdvertisingToLocator**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene il valore che indica se il servizio localizzatore nel controller di dominio sta annunci correttamente. **TRUE** se il servizio localizzatore nel controller di dominio sta annunci correttamente; in caso contrario, **FALSE.**

</dd> <dt>

**IsGC**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene il valore che indica se il controller di dominio è un server di catalogo globale. **TRUE** se il controller di dominio è un server di catalogo globale. in caso contrario, **FALSE.**

</dd> <dt>

**IsNextRIDPoolAvailable**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene il valore che indica se il controller di dominio ha ottenuto un altro pool di RID. **TRUE** se il controller di dominio ha ottenuto un altro pool di RID e l'allocazione di RID in questo controller di dominio può continuare anche se il pool corrente di RID è esaurito; in caso contrario, **FALSE.**

</dd> <dt>

**IsRegisteredInDNS**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene il valore che indica se il controller di dominio è registrato correttamente in DNS. **TRUE** se il controller di dominio è registrato correttamente in DNS. in caso contrario, **FALSE.**

</dd> <dt>

**IsSysVolReady**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene il valore che indica se SysVol è stato pubblicato correttamente. **TRUE** se SysVol è stato pubblicato correttamente. in caso contrario, **FALSE.**

</dd> <dt>

**NTDsaGUID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene il GUID associato all'oggetto [**NTDS-DSA**](/windows/desktop/ADSchema/c-ntdsdsa) nel contenitore di configurazione. **L'oggetto NTDS-DSA** rappresenta il Dominio di Active Directory DSA del servizio nel server.

</dd> <dt>

**PercentOfRIDsLeft**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene la percentuale di RID rimasti nel pool di RID corrente in questo controller di dominio.

</dd> <dt>

**Sitename**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene il sito in cui si trova il controller di dominio.

</dd> <dt>

**TimeOfOldestReplAdd**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene il timestamp dell'operazione di aggiunta della replica meno recente che si trova ancora nella coda in questo controller di dominio.

</dd> <dt>

**TimeOfOldestReplDel**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene il timestamp dell'operazione di eliminazione della replica meno recente ancora nella coda in questo controller di dominio.

</dd> <dt>

**TimeOfOldestReplMod**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene il timestamp dell'operazione di modifica della replica meno recente che si trova ancora nella coda in questo controller di dominio.

</dd> <dt>

**TimeOfOldestReplSync**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene il timestamp dell'operazione di sincronizzazione della replica meno recente ancora nella coda in questo controller di dominio.

</dd> <dt>

**TimeOfOldestReplUpdRefs**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene il timestamp dell'operazione di aggiornamento della replica meno recente ancora nella coda in questo controller di dominio.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | Radice \\ MicrosoftActiveDirectory<br/>                                               |
| MOF<br/>                      | <dl> <dt>Replprov.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Replprov.dll</dt> </dl> |



 

