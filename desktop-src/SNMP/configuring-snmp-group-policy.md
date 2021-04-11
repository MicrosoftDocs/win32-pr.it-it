---
title: Configurazione Criteri di gruppo SNMP
description: Se si utilizza lo snap-in Microsoft Management Console (MMC) per Criteri di gruppo per amministrare le impostazioni dei criteri basate sul Registro di sistema applicabili a SNMP, è possibile che esistano una o più delle sottochiavi seguenti.
ms.assetid: de21d2f5-3337-47ba-afcf-347e289873d3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 817797dbc0e67f6006e12751beca533cbbec3656
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118223"
---
# <a name="configuring-snmp-group-policy"></a>Configurazione Criteri di gruppo SNMP

Se si utilizza lo snap-in Microsoft Management Console (MMC) per Criteri di gruppo per amministrare le impostazioni dei criteri basate sul Registro di sistema applicabili a SNMP, è possibile che esistano una o più delle sottochiavi seguenti.

**HKEY \_ \_** \\  \\  \\  \\ **Parametri** SNMP dei criteri \\  software del computer locale ValidCommunities

**HKEY \_ \_** \\  \\  \\  \\ **Parametri** SNMP dei criteri \\  software del computer locale PermittedManagers

**HKEY \_ \_** \\  \\  \\  \\ **Parametri** SNMP dei criteri \\  software del computer locale TrapConfiguration

In genere, solo i membri del gruppo locale Administrators possono accedere alle sottochiavi del registro di sistema seguenti che archiviano i dati di configurazione per il servizio SNMP:

**HKEY \_ \_** \\  \\  \\  \\  \\ **Parametri** SNMP dei servizi \\  CurrentControlSet del sistema del computer locale ValidCommunities

**HKEY \_ \_** \\  \\  \\  \\  \\ **Parametri** SNMP dei servizi \\  CurrentControlSet del sistema del computer locale PermittedManagers

Per ulteriori informazioni sulle impostazioni dei criteri basate sul Registro di sistema, vedere [about criteri di gruppo](/previous-versions/windows/desktop/Policy/about-group-policy).

 

 