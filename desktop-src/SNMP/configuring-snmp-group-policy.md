---
title: Configurazione di SNMP Criteri di gruppo
description: Se si usa lo snap-in Microsoft Management Console (MMC) per Criteri di gruppo per amministrare le impostazioni dei criteri basate sul Registro di sistema applicabili a SNMP, possono esistere una o più delle sottochiavi seguenti.
ms.assetid: de21d2f5-3337-47ba-afcf-347e289873d3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e17bc3b1bac886a19791f57903920a11062072a81577a0a78ab01d461709ee3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009659"
---
# <a name="configuring-snmp-group-policy"></a>Configurazione di SNMP Criteri di gruppo

Se si usa lo snap-in Microsoft Management Console (MMC) per Criteri di gruppo per amministrare le impostazioni dei criteri basate sul Registro di sistema applicabili a SNMP, possono esistere una o più delle sottochiavi seguenti.

**HKEY \_ Local \_ MACHINE** \\ **SOFTWARE** \\ **Policies** \\ **SNMP** \\ **Parameters** \\ **ValidCommunities**

**HKEY \_ Parametri \_** \\  \\  \\ **SNMP** dei criteri SOFTWARE DELLA MACCHINA LOCALE \\  \\ **ConsentitiManager**

**HKEY \_ Local \_ MACHINE** \\ **SOFTWARE** \\ **Policies** \\ **SNMP** \\ **Parameters** \\ **TrapConfiguration**

In genere, solo i membri del gruppo locale Administrators possono accedere alle sottochiavi del Registro di sistema seguenti che archiviano i dati di configurazione per il servizio SNMP:

**HKEY \_ Local \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **SNMP** \\ **Parameters** \\ **ValidCommunities**

**HKEY \_ Local \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **SNMP** \\ **Parameters** \\ **PermittedManagers**

Per altre informazioni sulle impostazioni dei criteri basati sul Registro di sistema, vedere [Informazioni Criteri di gruppo](/previous-versions/windows/desktop/Policy/about-group-policy).

 

 