---
title: Proprietà di ITsSbTaskInfo
description: L'interfaccia ITsSbTaskInfo espone le proprietà seguenti.
ms.assetid: 402B8502-DE17-440B-867D-45922582C30E
ms.tgt_platform: multiple
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c0e4c8fefc2e443778b2ce177e61a314a3e0ef9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718283"
---
# <a name="itssbtaskinfo-properties"></a>Proprietà di ITsSbTaskInfo

L'interfaccia [**ITsSbTaskInfo**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskinfo) espone le proprietà seguenti.

## <a name="in-this-section"></a>Contenuto della sezione

<dl> <dt>

[**Proprietà di contesto**](itssbtaskinfo-context.md)
</dt> <dd>

Recupera i byte del contesto associati all'attività.

</dd> <dt>

[**Proprietà scadenza**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_deadline)
</dt> <dd>

Recupera l'ora in cui l'attività deve essere avviata. Viene usato per assegnare priorità alle patch. Per prima cosa viene avviata la patch con la prima scadenza.

</dd> <dt>

[**Proprietà EndTime**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_endtime)
</dt> <dd>

Recupera l'ultima volta che l'agente attività è in grado di avviare l'attività.

</dd> <dt>

[**Proprietà Identificatore**](itssbtaskinfo-identifier.md)
</dt> <dd>

Recupera un GUID utilizzato come identificatore univoco da parte dell'agente attività.

</dd> <dt>

[**proprietà Label**](itssbtaskinfo-label.md)
</dt> <dd>

Recupera l'etichetta che descrive lo scopo dell'attività.

</dd> <dt>

[**Proprietà del plug-in**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_plugin)
</dt> <dd>

Recupera il nome visualizzato dell'agente attività.

</dd> <dt>

[**StartTime (proprietà)**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_starttime)
</dt> <dd>

Recupera la prima volta che l'agente attività è in grado di avviare l'attività.

</dd> <dt>

[**Status (proprietà)**](itssbtaskinfo-status.md)
</dt> <dd>

Recupera un valore di enumerazione [**\_ \_ dello stato dell'attività RDV**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status) che rappresenta lo stato dell'attività.

</dd> <dt>

[**Proprietà TargetId**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_targetid)
</dt> <dd>

Recupera l'identificatore di destinazione.

</dd> </dl>

 

 




