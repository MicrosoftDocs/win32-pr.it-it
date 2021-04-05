---
description: Descrive il formato di data e ora Common Information Model (CIM) utilizzato da WMI. Questo formato è indipendente dalle impostazioni locali, quindi gli script che usano DATETIME possono essere eseguiti in molti fusi orari.
ms.assetid: be239bf8-88a3-47bc-ae4f-49a5195e7a7d
ms.tgt_platform: multiple
title: Formato di data e ora
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a29e8f97930efa33942fe87b2109aa7cd7ba9d93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131159"
---
# <a name="date-and-time-format"></a>Formato di data e ora

WMI usa i formati di data e ora definiti dalla specifica[DMTF.org](https://www.dmtf.org/)(Distributed Management Task Force) Common Information Model (CIM).

Il **formato \_ DateTime CIM** viene implementato in Microsoft [Managed Object Format (MOF)](managed-object-format--mof-.md) dal tipo di dati MOF [DateTime](datetime.md) . I formati di data e ora possono inoltre esprimere un intervallo di tempo.

Per ulteriori informazioni sui formati WMI, vedere [CIM \_ DateTime](cim-datetime.md) and [Interval Format](interval-format.md).

Per ulteriori informazioni sulla conversione da e verso il formato DATETIME WMI, vedere [**SWbemDateTime**](swbemdatetime.md) e l'articolo su TechNet ScriptCenter [it about time (Oh e about dates)](https://www.microsoft.com/technet/technetmag/issues/2006/07/ScriptingGuy/default.aspx).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su WMI](about-wmi.md)
</dt> </dl>

 

 



