---
title: MSAD_ReplCursor classe
description: Fornisce informazioni sullo stato della replica in ingresso su tutte le repliche di un determinato contesto dei nomi (NC).
ms.assetid: 5746cfe9-b113-4be3-b609-15cb937c271b
ms.tgt_platform: multiple
keywords:
- MSAD_ReplCursor classe Active Directory
- MSAD_ReplCursor classe Active Directory , descritto
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
ms.openlocfilehash: c001adf774321ba61e232298d070fb4a29d4b3f0740dd8ef900ff4ea0b4cb83a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118186066"
---
# <a name="msad_replcursor-class"></a>Classe \_ MSAD ReplCursor

Fornisce informazioni sullo stato della replica in ingresso su tutte le repliche di un determinato contesto dei nomi (NC).

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

La **classe MSAD \_ ReplCursor** include questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe MSAD \_ ReplCursor** ha queste proprietà.

<dl> <dt>

**NamingContextDN**
</dt> <dd> <dl> <dt>

Tipo di dati: **Stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Ottiene il percorso X.500 per il contesto dei nomi (NC) che contiene questo cursore.

</dd> <dt>

**SourceDsaDN**
</dt> <dd> <dl> <dt>

Tipo di dati: **Stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene il percorso X.500 per l'agente del sistema di directory (DSA) che rappresenta il controller di dominio di origine.

</dd> <dt>

**SourceDsaInvocationID**
</dt> <dd> <dl> <dt>

Tipo di dati: **Stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Ottiene l'identificatore di chiamata del server di origine a cui **corrisponde USNAttributeFilter.**

</dd> <dt>

**TimeOfLastSuccessfulSync**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene il timestamp dell'ultima sincronizzazione della replica riuscita con il DSA di origine. Indica l'ora dell'ultima volta in cui questo controller di dominio ha visto le modifiche apportate al DSA di origine per questo NC.

</dd> <dt>

**USNAttributeFilter**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene il numero massimo di sequenza di aggiornamento a cui il server di destinazione può indicare di avere registrato tutte le modifiche originate dal server specificato in numeri di sequenza di aggiornamento minori o uguali a questo numero di sequenza di aggiornamento. Questa proprietà viene usata per filtrare le modifiche già applicate dal server di destinazione nei server di origine della replica.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | Radice \\ MicrosoftActiveDirectory<br/>                                               |
| MOF<br/>                      | <dl> <dt>Replprov.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Replprov.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CURSORE REPL DS \_ \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursor)
</dt> </dl>

 

