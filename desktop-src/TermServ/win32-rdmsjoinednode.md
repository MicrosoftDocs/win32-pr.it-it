---
title: Classe Win32_RDMSJoinedNode
description: Rappresenta un nodo del server gestito da Desktop remoto Management Services (RDBMS).
ms.assetid: 8751f3f7-dfb5-45bd-a6b1-758aa22a3569
ms.tgt_platform: multiple
keywords:
- Classe Win32_RDMSJoinedNode Servizi Desktop remoto
- Classe Win32_RDMSJoinedNode Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_RDMSJoinedNode
- Win32_RDMSJoinedNode.FQDN
- Win32_RDMSJoinedNode.SID
- Win32_RDMSJoinedNode.OSVersion
- Win32_RDMSJoinedNode.IsRdcb
- Win32_RDMSJoinedNode.IsRdg
- Win32_RDMSJoinedNode.IsRdls
- Win32_RDMSJoinedNode.IsRdvh
- Win32_RDMSJoinedNode.IsRdwa
- Win32_RDMSJoinedNode.IsRdsh
- Win32_RDMSJoinedNode.IsWebAccessCertificateInstalled
- Win32_RDMSJoinedNode.IsGatewayCertificateInstalled
- Win32_RDMSJoinedNode.IsRedirectorCertificateInstalled
- Win32_RDMSJoinedNode.IsPublishingCertificateInstalled
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cabf1cf7ff98b698624285b2877412c4323259b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400276"
---
# <a name="win32_rdmsjoinednode-class"></a>Win32 \_ RDMSJoinedNode (classe)

Rappresenta un nodo del server gestito da Desktop remoto Management Services (RDBMS).

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSJoinedNode
{
  string  FQDN;
  string  SID;
  String  OSVersion;
  boolean IsRdcb;
  boolean IsRdg;
  boolean IsRdls;
  boolean IsRdvh;
  boolean IsRdwa;
  boolean IsRdsh;
  boolean IsWebAccessCertificateInstalled;
  boolean IsGatewayCertificateInstalled;
  boolean IsRedirectorCertificateInstalled;
  boolean IsPublishingCertificateInstalled;
};
```

## <a name="members"></a>Members

La classe **Win32 \_ RDMSJoinedNode** presenta questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La classe **Win32 \_ RDMSJoinedNode** presenta questi metodi.



| Metodo                                                                | Descrizione                                                                                                                                                                                           |
|:----------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetJoinedNodeCount**](win32-rdmsjoinednode-getjoinednodecount.md) | **Windows server 2012 R2 e Windows server 2012:** Questo metodo non è disponibile prima di Windows Server 2016.<br/> Ottiene il numero di server in cui è installato il ruolo specificato.<br/> |
| [**Partecipa**](join-win32-rdmsjoinednode.md)                             | Aggiunge un nodo a RDBMS.<br/>                                                                                                                                                                       |
| [**Separazione**](unjoin-win32-rdmsjoinednode.md)                         | Rimuove un nodo da RDBMS.<br/>                                                                                                                                                                  |



 

### <a name="properties"></a>Proprietà

La classe **Win32 \_ RDMSJoinedNode** dispone di queste proprietà.

<dl> <dt>

**Nome di dominio completo**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Ottiene il nome di dominio completo del nodo.

</dd> <dt>

**IsGatewayCertificateInstalled**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Ottiene e imposta un valore che indica se il server dispone di un certificato per eseguire l'autenticazione per le connessioni del Gateway Desktop remoto. **True** se il certificato è installato; in caso contrario, **false**.

</dd> <dt>

**IsPublishingCertificateInstalled**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Ottiene e imposta un valore che indica se il server dispone di un certificato per firmare i file di pubblicazione Remote Desktop Protocol. **True** se il certificato è installato; in caso contrario, **false**.

</dd> <dt>

**IsRdcb**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Ottiene e imposta un valore che indica se il server è Connessione Desktop remoto broker. **True** se il server è un Broker di connessione Desktop remoto; in caso contrario, **false**.

</dd> <dt>

**IsRdg**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Ottiene e imposta un valore che indica se il server è Desktop remoto server gateway. **True** se il server è un server Gateway Desktop remoto; in caso contrario, **false**.

</dd> <dt>

**IsRdls**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Ottiene e imposta un valore che indica se il server è Desktop remoto server licenze. **True** se il server è un server licenze Desktop remoto; in caso contrario, **false**.

</dd> <dt>

**IsRdsh**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Ottiene e imposta un valore che indica se il server è Desktop remoto server Host sessione. **True** se il server è un server Host sessione di desktop remoto; in caso contrario, **false**.

</dd> <dt>

**IsRdvh**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Ottiene e imposta un valore che indica se il server è Desktop remoto host di virtualizzazione. **True** se il server è un host di virtualizzazione Desktop remoto; in caso contrario, **false**.

</dd> <dt>

**IsRdwa**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Ottiene e imposta un valore che indica se il server è Desktop remoto server Accesso Web. **True** se il server è un desktop remoto accesso Web Server; in caso contrario, **false**.

</dd> <dt>

**IsRedirectorCertificateInstalled**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Ottiene e imposta un valore che indica se il server dispone di un certificato per eseguire l'autenticazione per la distribuzione di Servizi Desktop remoto. **True** se il certificato è installato; in caso contrario, **false**.

</dd> <dt>

**IsWebAccessCertificateInstalled**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Ottiene e imposta un valore che indica se il server dispone di un certificato per eseguire l'autenticazione per Desktop remoto Accesso Web. **True** se il certificato è installato; in caso contrario, **false**.

</dd> <dt>

**OSVersion**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Ottiene e imposta la versione dei sistemi operativi nel nodo.

</dd> <dt>

**SID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Ottiene l'ID di sicurezza (SID) del nodo.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                   |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                              |
| Spazio dei nomi<br/>                | Radice \\ CIMV2 \\ RDBMS<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Provider di Desktop remoto Management Services](rdms-api-reference.md)
</dt> </dl>

 

