---
title: Classe Win32_RDMSPublishedApplication
description: Gestisce un'applicazione pubblicata.
ms.assetid: 7a529f1d-1aaf-42fb-8469-92d38a7b0ffc
ms.tgt_platform: multiple
keywords:
- Classe Win32_RDMSPublishedApplication Servizi Desktop remoto
- Classe Win32_RDMSPublishedApplication Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_RDMSPublishedApplication
- Win32_RDMSPublishedApplication.AppAlias
- Win32_RDMSPublishedApplication.PoolName
- Win32_RDMSPublishedApplication.DisplayName
- Win32_RDMSPublishedApplication.ShowInPortal
- Win32_RDMSPublishedApplication.SecurityDescriptor
- Win32_RDMSPublishedApplication.AppPath
- Win32_RDMSPublishedApplication.VirtualPath
- Win32_RDMSPublishedApplication.CommandLineSetting
- Win32_RDMSPublishedApplication.RequiredCommandLine
- Win32_RDMSPublishedApplication.Folder
- Win32_RDMSPublishedApplication.IconPath
- Win32_RDMSPublishedApplication.IconIndex
- Win32_RDMSPublishedApplication.IconContents
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb003faf5e51c9da1f46f23c5f8d6b5ae977987c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341123"
---
# <a name="win32_rdmspublishedapplication-class"></a>Win32 \_ RDMSPublishedApplication (classe)

Gestisce un'applicazione pubblicata.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSPublishedApplication
{
  string  AppAlias;
  string  PoolName;
  string  DisplayName;
  boolean ShowInPortal;
  string  SecurityDescriptor;
  string  AppPath;
  string  VirtualPath;
  uint32  CommandLineSetting;
  string  RequiredCommandLine;
  string  Folder;
  string  IconPath;
  sint32  IconIndex;
  uint8   IconContents[];
};
```

## <a name="members"></a>Members

La classe **Win32 \_ RDMSPublishedApplication** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **Win32 \_ RDMSPublishedApplication** dispone di queste proprietà.

<dl> <dt>

**AppAlias**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Ottiene e imposta l'alias dell'applicazione.

</dd> <dt>

**AppPath**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Ottiene e imposta il percorso dell'applicazione.

</dd> <dt>

**CommandLineSetting**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Ottiene e imposta l'impostazione della riga di comando per l'applicazione.

Questa proprietà può essere impostata su uno dei valori seguenti:

<dt>

<span id="DoNotAllow"></span><span id="donotallow"></span><span id="DONOTALLOW"></span>

<span id="DoNotAllow"></span><span id="donotallow"></span><span id="DONOTALLOW"></span>**DoNotAllow** (0)


</dt> <dd>

Non consentire argomenti della riga di comando.

</dd> <dt>

<span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>

<span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>**Consenti** (1)


</dt> <dd>

Consente argomenti della riga di comando.

</dd> <dt>

<span id="Require"></span><span id="require"></span><span id="REQUIRE"></span>

<span id="Require"></span><span id="require"></span><span id="REQUIRE"></span>**Richiedi** (2)


</dt> <dd>

Richiedere argomenti della riga di comando.

</dd> </dl>

</dd> <dt>

**DisplayName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Ottiene e imposta il nome visualizzato dell'applicazione.

</dd> <dt>

**Cartella**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Ottiene e imposta il percorso dell'applicazione.

</dd> <dt>

**IconContents**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **Uint8**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Ottiene e imposta una matrice che contiene l'icona dell'applicazione.

</dd> <dt>

**IconIndex**
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Ottiene e imposta l'indice per l'icona dell'applicazione.

</dd> <dt>

**IconPath**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Ottiene e imposta il percorso dell'icona per l'applicazione.

</dd> <dt>

**PoolName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Ottiene e imposta il nome del pool di applicazioni dell'applicazione.

</dd> <dt>

**RequiredCommandLine**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Ottiene e imposta gli argomenti della riga di comando necessari per l'applicazione.

</dd> <dt>

**SecurityDescriptor**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [ **facoltativo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Ottiene e imposta il descrittore di sicurezza che controlla l'accesso all'applicazione nel formato SDDL (Security Descriptor Definition Language).

</dd> <dt>

**ShowInPortal**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Indica se visualizzare l'applicazione in Servizi terminal Accesso Web (Accesso Web TS). **True** per visualizzare l'applicazione in accesso Web di Servizi terminal; in caso contrario, **false**.

</dd> <dt>

**VirtualPath**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Ottiene e imposta il percorso virtuale dell'applicazione.

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

 

