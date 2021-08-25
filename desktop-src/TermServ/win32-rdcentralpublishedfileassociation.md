---
title: Win32_RDCentralPublishedFileAssociation classe
description: Informazioni per un'estensione di file associata a un'applicazione.
ms.assetid: ba12d933-572c-48d3-bf0f-1c99de61457d
ms.tgt_platform: multiple
keywords:
- Win32_RDCentralPublishedFileAssociation classe Servizi Desktop remoto
- Win32_RDCentralPublishedFileAssociation classe Servizi Desktop remoto , descritto
topic_type:
- apiref
api_name:
- Win32_RDCentralPublishedFileAssociation
- Win32_RDCentralPublishedFileAssociation.ExtName
- Win32_RDCentralPublishedFileAssociation.AppAlias
- Win32_RDCentralPublishedFileAssociation.FarmAlias
- Win32_RDCentralPublishedFileAssociation.ProgIdHint
- Win32_RDCentralPublishedFileAssociation.IconContents
- Win32_RDCentralPublishedFileAssociation.PrimaryHandler
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41361959c56810036b8ca2e17d338e2ff1d3433c6e0384fd168a2d21d6e0e0f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119868451"
---
# <a name="win32_rdcentralpublishedfileassociation-class"></a>Classe \_ RDCentralPublishedFileAssociation Win32

Informazioni per un'estensione di file associata a un'applicazione

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[dynamic, provider("Win32_TSCentralPublisher_Prov")]
class Win32_RDCentralPublishedFileAssociation
{
  string  ExtName;
  string  AppAlias;
  string  FarmAlias;
  string  ProgIdHint;
  uint8   IconContents[];
  boolean PrimaryHandler;
};
```

## <a name="members"></a>Members

La **classe \_ WIN32 RDCentralPublishedFileAssociation** include questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe WIN32 \_ RDCentralPublishedFileAssociation** ha queste proprietà.

<dl> <dt>

**AppAlias**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Alias dell'applicazione RemoteApp dell'associazione di file.

</dd> <dt>

**ExtName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> <dt>

Qualificatori: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nome dell'estensione,ad esempio .txt.

</dd> <dt>

**FarmAlias**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Alias della farm di RemoteApp dell'associazione file

</dd> <dt>

**IconContents**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint8**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Contenuto dell'icona per questa associazione di file.

</dd> <dt>

**PrimaryHandler**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Riservato per utilizzi futuri. Sarà sempre **true.**

</dd> <dt>

**ProgIdHint**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Suggerimento per consentire l'apertura di documenti con questa associazione di file.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                           |
| Spazio dei nomi<br/>                | Radice \\ cimv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>Tscpub.mof</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>TscPubWmi.dll</dt> </dl> |



 

