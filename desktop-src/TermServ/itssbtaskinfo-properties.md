---
title: Proprietà ITsSbTaskInfo
description: L'interfaccia ITsSbTaskInfo espone le proprietà seguenti.
ms.assetid: 402B8502-DE17-440B-867D-45922582C30E
ms.tgt_platform: multiple
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d91b24b95b6b19cb439350c0c6823306c66a8fab5fe47f0f9e9fb739df64e3cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118128069"
---
# <a name="itssbtaskinfo-properties"></a>Proprietà ITsSbTaskInfo

[**L'interfaccia ITsSbTaskInfo**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskinfo) espone le proprietà seguenti.

## <a name="in-this-section"></a>Contenuto della sezione

<dl> <dt>

[**Proprietà Context**](itssbtaskinfo-context.md)
</dt> <dd>

Recupera i byte di contesto associati all'attività.

</dd> <dt>

[**Proprietà Deadline**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_deadline)
</dt> <dd>

Recupera l'ora entro la quale deve essere avviata l'attività. Viene usato per classificare le patch in ordine di priorità. La patch con la scadenza meno recente verrà avviata per prima.

</dd> <dt>

[**Proprietà EndTime**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_endtime)
</dt> <dd>

Recupera l'ora più recente in cui l'agente attività può avviare l'attività.

</dd> <dt>

[**Proprietà Identificatore**](itssbtaskinfo-identifier.md)
</dt> <dd>

Recupera un GUID utilizzato come identificatore univoco dall'agente attività.

</dd> <dt>

[**proprietà Label**](itssbtaskinfo-label.md)
</dt> <dd>

Recupera l'etichetta che descrive lo scopo dell'attività.

</dd> <dt>

[**Proprietà del plug-in**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_plugin)
</dt> <dd>

Recupera il nome visualizzato dell'agente attività.

</dd> <dt>

[**Proprietà StartTime**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_starttime)
</dt> <dd>

Recupera il primo momento in cui l'agente attività può avviare l'attività.

</dd> <dt>

[**Status (proprietà)**](itssbtaskinfo-status.md)
</dt> <dd>

Recupera un valore [**di enumerazione RDV \_ TASK \_ STATUS**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status) che rappresenta lo stato dell'attività.

</dd> <dt>

[**Proprietà TargetId**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_targetid)
</dt> <dd>

Recupera l'identificatore di destinazione.

</dd> </dl>

 

 




