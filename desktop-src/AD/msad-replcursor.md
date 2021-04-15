---
title: Classe MSAD_ReplCursor
description: Fornisce informazioni sullo stato di replica in ingresso su tutte le repliche di un determinato contesto dei nomi (NC).
ms.assetid: 5746cfe9-b113-4be3-b609-15cb937c271b
ms.tgt_platform: multiple
keywords:
- Classe MSAD_ReplCursor Active Directory
- Classe MSAD_ReplCursor Active Directory, descritta
topic_type:
- apiref
api_name:
- MSAD_ReplCursor
- MSAD_ReplCursor.NamingContextDN
- MSAD_ReplCursor.SourceDsaInvocationID
- MSAD_ReplCursor.USNAttributeFilter
- MSAD_ReplCursor.SourceDsaDN
- MSAD_ReplCursor.TimeOfLastSuccessfulSync
api_location:
- replprov.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f725ac8e9eee9f921ce4109e0b0e42ed85e75ab8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476846"
---
# <a name="msad_replcursor-class"></a>\_Classe MSAD ReplCursor

Fornisce informazioni sullo stato di replica in ingresso su tutte le repliche di un determinato contesto dei nomi (NC).

## <a name="syntax"></a>Sintassi

``` syntax
[dynamic, provider("ReplProv1")]
class MSAD_ReplCursor
{
  String   NamingContextDN;
  String   SourceDsaInvocationID;
  uint64   USNAttributeFilter;
  String   SourceDsaDN;
  datetime TimeOfLastSuccessfulSync;
};
```

## <a name="members"></a>Members

La **classe \_ ReplCursor di MSAD** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ ReplCursor di MSAD** dispone di queste proprietà.

<dl> <dt>

**NamingContextDN**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Ottiene il percorso X. 500 per il contesto dei nomi (NC) che include il cursore.

</dd> <dt>

**SourceDsaDN**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene il percorso X. 500 per il Directory System Agent (DSA) che rappresenta il controller di dominio di origine (DC).

</dd> <dt>

**SourceDsaInvocationID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Ottiene l'identificatore di chiamata del server di origine a cui corrisponde l'oggetto **USNAttributeFilter** .

</dd> <dt>

**TimeOfLastSuccessfulSync**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene il timestamp dell'ultima sincronizzazione corretta della replica con il DSA di origine. Indica l'ora in cui il controller di dominio ha rilevato le modifiche apportate nell'origine DSA per questo NC.

</dd> <dt>

**USNAttributeFilter**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene il numero di sequenza di aggiornamento massimo a cui il server di destinazione può indicare che ha registrato tutte le modifiche originate dal server specificato in corrispondenza dei numeri di sequenza di aggiornamento minori o uguali a questo numero di sequenza dell'aggiornamento. Questa proprietà viene utilizzata per filtrare le modifiche che il server di destinazione ha già applicato ai server di origine della replica.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\MicrosoftActiveDirectory radice<br/>                                               |
| MOF<br/>                      | <dl> <dt>Replprov. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Replprov.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_cursore REPL \_ DS**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursor)
</dt> </dl>

 

