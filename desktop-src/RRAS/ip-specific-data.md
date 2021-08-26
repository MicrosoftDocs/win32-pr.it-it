---
title: IP_SPECIFIC_DATA struttura (Rtm.h)
description: La struttura \_ IP SPECIFIC DATA contiene dati specifici dell'IP.
ms.assetid: 68f2f4cc-141b-4f22-94ac-cc72e8dcca0a
keywords:
- IP_SPECIFIC_DATA struttura RAS
- PIP_SPECIFIC_DATA puntatore alla struttura RAS
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
ms.openlocfilehash: 906ae9f2accb3d380227f08ad6b65642b96ce6bfa928591bd11a69c478f531b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120036671"
---
# <a name="ip_specific_data-structure"></a>Struttura \_ DEI DATI SPECIFICI \_ DELL'INDIRIZZO IP

\[Questa API è stata sostituita dall'API Gestione tabelle di [routing versione 2](about-routing-table-manager-version-2.md) e non sarà disponibile oltre Windows Server 2003. Le applicazioni devono usare l'API Gestione tabelle di routing versione 2.\]

La **struttura IP SPECIFIC \_ DATA** contiene dati specifici dell'IP.

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

**Tipo \_ FSD**
</dt> <dd>

Specifica il tipo di route come definito in [RFC 1354.](routing-protocols-request-for-comments.md) La tabella seguente illustra i valori possibili per questo membro.



| Membro                                                                                               | Significato                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Il tipo di route non è specificato. Il tipo è diverso da quelli elencati qui.<br/>                                                                                                                                                                                         |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | La route non è valida. In genere, questo valore viene usato per invalidare una route. Tuttavia, poiché l'invalidazione non è supportata dal gestore tabelle di routing, la route viene comunque considerata nei calcoli best-route. Pertanto, i protocolli di routing non devono usare questo valore.<br/> |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | La route è una route locale, cio' l'hop successivo è la destinazione finale.<br/>                                                                                                                                                                                            |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | La route è una route remota, ad esempio l'hop successivo non è la destinazione finale.<br/>                                                                                                                                                                                       |



 

</dd> <dt>

**Criteri \_ FSD**
</dt> <dd>

Specifica il set di condizioni che causerebbe la selezione di una route a più percorsi. Questo membro è in genere in formato TOS IP. Per altre informazioni, vedere [RFC 1354](routing-protocols-request-for-comments.md).

</dd> <dt>

**FSD \_ NextHopAS**
</dt> <dd>

Specifica il numero di sistema autonomo dell'hop successivo.

</dd> <dt>

**Priorità \_ FSD**
</dt> <dd>

Specifica un valore della metrica. Il gestore tabelle di routing usa questo valore per confrontare questa voce di route con le voci di route ottenute da altri protocolli di routing. Il valore di questo membro viene impostato dal gestore tabelle di routing.

</dd> <dt>

**Metrica \_ FSD**
</dt> <dd>

Specifica un valore della metrica. Il gestore tabelle di routing usa questo valore per confrontare questa voce di route con altre voci di route ottenute dallo stesso protocollo di routing. Il valore di questo membro viene impostato dal protocollo di routing.

</dd> <dt>

**Metrica \_ FSD1**
</dt> <dd>

Specifica un valore di metrica specifico del protocollo di routing. Questo valore della metrica è documentato in [RFC 1354.](routing-protocols-request-for-comments.md)

</dd> <dt>

**Metrica \_ FSD 2**
</dt> <dd>

Specifica un valore di metrica specifico del protocollo di routing. Questo valore della metrica è documentato in [RFC 1354.](routing-protocols-request-for-comments.md)

</dd> <dt>

**Metrica \_ FSD3**
</dt> <dd>

Specifica un valore di metrica specifico del protocollo di routing. Questo valore della metrica è documentato in [RFC 1354.](routing-protocols-request-for-comments.md)

</dd> <dt>

**Metrica \_ FSD4**
</dt> <dd>

Specifica un valore di metrica specifico del protocollo di routing. Questo valore della metrica è documentato in [RFC 1354.](routing-protocols-request-for-comments.md)

</dd> <dt>

**Metrica \_ FSD5**
</dt> <dd>

Specifica un valore di metrica specifico del protocollo di routing. Questo valore della metrica è documentato in [RFC 1354.](routing-protocols-request-for-comments.md)

</dd> <dt>

**Flag \_ FSD**
</dt> <dd>

Specifica se la route è valida. Il protocollo di routing deve prima cancellare questi flag e quindi impostare la route come valida o non valida. Il protocollo di routing deve usare le macro **ClearRouteFlags(),** **SetRouteValid()** e **ClearRouteValid()** per eseguire queste operazioni. Queste macro sono definite in Rtm.h.

</dd> </dl>

## <a name="remarks"></a>Commenti

Gestione tabelle di routing usa i **membri Priorità \_ FSD** e Metrica **FSD \_** per calcolare la route migliore verso una determinata rete di destinazione.

I **membri della \_ metrica \[ FSD 1-5 \]** sono conformi a MIB II. Gli agenti MIB II visualizzano solo questi valori delle metriche. Non visualizzano il **valore della metrica FSD \_ Metric.** Per visualizzare la **metrica FSD, \_** il protocollo di routing deve archiviare anche il valore in uno dei membri della metrica **FSD \_ \[ 1-5. \]**

Gestione tabelle di routing non usa i valori delle metriche nei membri della metrica **FSD da 1 a \_ \[ 5 \]** quando si calcola la route migliore verso una rete di destinazione. Pertanto, il protocollo di routing deve garantire che il **membro \_ della** metrica FSD abbia un valore di metrica appropriato.

Un protocollo di routing potrebbe usare i **flag FSD \_** per contrassegnare una route come non valida, se la route non deve essere usata da altri protocolli di routing.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                        |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                   |
| Intestazione<br/>                   | <dl> <dt>Rtm.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Informazioni di riferimento su Gestione tabelle di routing versione 1](routing-table-manager-version-1-reference.md)
</dt> <dt>

[Strutture di Gestione tabelle di routing versione 1](routing-table-manager-version-1-structures.md)
</dt> <dt>

[**RTM \_ IP \_ ROUTE**](rtm-ip-route.md)
</dt> </dl>

 

 





