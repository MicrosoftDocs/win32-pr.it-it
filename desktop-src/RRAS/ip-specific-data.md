---
title: Struttura IP_SPECIFIC_DATA (RTM. h)
description: La \_ struttura dei dati specifici dell'IP contiene dati specifici dell'IP.
ms.assetid: 68f2f4cc-141b-4f22-94ac-cc72e8dcca0a
keywords:
- RAS struttura IP_SPECIFIC_DATA
- RAS puntatore alla struttura PIP_SPECIFIC_DATA
topic_type:
- apiref
api_name:
- IP_SPECIFIC_DATA
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a3ed319f7cf42295bf918ed3ec67f5d59fe5d80
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120435"
---
# <a name="ip_specific_data-structure"></a>\_ \_ Struttura dati specifica IP

\[Questa API è stata sostituita dall'API di [Gestione tabelle di routing versione 2](about-routing-table-manager-version-2.md) e non sarà disponibile oltre Windows Server 2003. Le applicazioni devono usare l'API di Routing Table Manager versione 2.\]

La **struttura \_ dei dati specifici dell'IP** contiene dati specifici dell'IP.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _IP_SPECIFIC_DATA {
  DWORD FSD_Type;
  DWORD FSD_Policy;
  DWORD FSD_NextHopAS;
  DWORD FSD_Priority;
  DWORD FSD_Metric;
  DWORD FSD_Metric1;
  DWORD FSD_Metric2;
  DWORD FSD_Metric3;
  DWORD FSD_Metric4;
  DWORD FSD_Metric5;
  DWORD FSD_Flags;
} IP_SPECIFIC_DATA, *PIP_SPECIFIC_DATA;
```



## <a name="members"></a>Members

<dl> <dt>

**\_Tipo FSD**
</dt> <dd>

Specifica il tipo di route come definito nella [specifica RFC 1354](routing-protocols-request-for-comments.md). Nella tabella seguente sono riportati i valori possibili per il membro.



| Membro                                                                                               | Significato                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Il tipo di route non è specificato. Il tipo è diverso da quelli elencati di seguito.<br/>                                                                                                                                                                                         |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Route non valida. In genere, questo valore viene usato per invalidare una route. Tuttavia, poiché l'invalidamento non è supportato da Gestione tabelle di routing, la route viene ancora considerata nei calcoli con la migliore route. Pertanto, i protocolli di routing non devono usare questo valore.<br/> |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | La route è una route locale, ovvero l'hop successivo è la destinazione finale.<br/>                                                                                                                                                                                            |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | La route è una route remota, ovvero l'hop successivo non è la destinazione finale.<br/>                                                                                                                                                                                       |



 

</dd> <dt>

**\_Criteri FSD**
</dt> <dd>

Specifica il set di condizioni che causerebbero la selezione di una route a percorsi multipli. Questo membro è in genere in formato IP TOS. Per ulteriori informazioni, vedere [RFC 1354](routing-protocols-request-for-comments.md).

</dd> <dt>

**\_NEXTHOPAS FSD**
</dt> <dd>

Specifica il numero di sistema autonomo dell'hop successivo.

</dd> <dt>

**\_Priorità FSD**
</dt> <dd>

Specifica un valore della metrica. Gestione tabelle di routing utilizza questo valore per confrontare questa voce di route con le voci di route ottenute da altri protocolli di routing. Il valore di questo membro viene impostato da Gestione tabelle di routing.

</dd> <dt>

**\_Metrica FSD**
</dt> <dd>

Specifica un valore della metrica. Gestione tabelle di routing utilizza questo valore per confrontare questa voce di route con altre voci di route ottenute dallo stesso protocollo di routing. Il valore di questo membro viene impostato dal protocollo di routing.

</dd> <dt>

**\_METRIC1 FSD**
</dt> <dd>

Specifica un valore di metrica specifico del protocollo di routing. Questo valore della metrica è documentato nella [RFC 1354](routing-protocols-request-for-comments.md).

</dd> <dt>

**\_METRIC2 FSD**
</dt> <dd>

Specifica un valore di metrica specifico del protocollo di routing. Questo valore della metrica è documentato nella [RFC 1354](routing-protocols-request-for-comments.md).

</dd> <dt>

**\_METRIC3 FSD**
</dt> <dd>

Specifica un valore di metrica specifico del protocollo di routing. Questo valore della metrica è documentato nella [RFC 1354](routing-protocols-request-for-comments.md).

</dd> <dt>

**\_METRIC4 FSD**
</dt> <dd>

Specifica un valore di metrica specifico del protocollo di routing. Questo valore della metrica è documentato nella [RFC 1354](routing-protocols-request-for-comments.md).

</dd> <dt>

**\_METRICA5 FSD**
</dt> <dd>

Specifica un valore di metrica specifico del protocollo di routing. Questo valore della metrica è documentato nella [RFC 1354](routing-protocols-request-for-comments.md).

</dd> <dt>

**\_Flag FSD**
</dt> <dd>

Specifica se la route è valida. Il protocollo di routing deve prima cancellare questi flag, quindi impostare la route come valida o non valida. Per eseguire queste operazioni, il protocollo di routing deve usare le macro **ClearRouteFlags ()**, **SetRouteValid ()** e **ClearRouteValid ()** . Queste macro sono definite in RTM. h.

</dd> </dl>

## <a name="remarks"></a>Commenti

Gestione tabelle di routing utilizza i membri della **\_ metrica** **FSD \_ Priority** e FSD per calcolare la migliore route a una determinata rete di destinazione.

I membri della **\_ metrica FSD \[ 1-5 \]** sono per la conformità a MIB II. Gli agenti MIB II visualizzano solo questi valori di metrica. Non visualizzano il valore della metrica della **\_ metrica FSD** . Per visualizzare la **\_ metrica FSD** , il protocollo di routing deve archiviare anche il valore in uno dei membri **della \_ metrica \[ FSD \] 1-5** .

Gestione tabelle di routing non usa i valori delle metriche nei membri **della \_ metrica \[ FSD \] 1-5** durante il calcolo della migliore route a una rete di destinazione. Il protocollo di routing deve pertanto garantire che il membro della **\_ metrica FSD** disponga di un valore di metrica appropriato.

Un protocollo di routing può utilizzare **i \_ flag FSD** per contrassegnare una route come non valida, se la route non deve essere utilizzata da altri protocolli di routing.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                        |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                   |
| Intestazione<br/>                   | <dl> <dt>RTM. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Riferimento di gestione tabelle di routing versione 1](routing-table-manager-version-1-reference.md)
</dt> <dt>

[Strutture di gestione tabelle di routing versione 1](routing-table-manager-version-1-structures.md)
</dt> <dt>

[**\_route IP \_ RTM**](rtm-ip-route.md)
</dt> </dl>

 

 





