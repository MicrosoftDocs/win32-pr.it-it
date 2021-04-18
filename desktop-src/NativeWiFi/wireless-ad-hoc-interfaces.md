---
description: L'interfaccia di programmazione ad hoc wireless è costituita dalle interfacce seguenti.
ms.assetid: 8e975750-cfcc-4e36-a3d1-539b7c077459
title: Interfacce ad hoc wireless
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcc4fe481a5be1ff428396e5fd9b199f5a291fbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309438"
---
# <a name="wireless-ad-hoc-interfaces"></a>Interfacce ad hoc wireless

L'interfaccia di programmazione ad hoc wireless è costituita dalle interfacce seguenti.



| Interface Name (Nome interfaccia)                                                                       | Descrizione                                                                                            |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**IDot11AdHocInterface**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocinterface)                                 | Rappresenta una scheda di interfaccia di rete wireless (NIC).                                                    |
| [**IDot11AdHocInterfaceNotificationSink**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocinterfacenotificationsink) | Definisce le notifiche supportate da [**IDot11AdHocInterface**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocinterface).           |
| [**IDot11AdHocManager**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocmanager)                                     | Crea e gestisce 802,11 reti ad hoc.                                                            |
| [**IDot11AdHocManagerNotificationSink**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocmanagernotificationsink)     | Definisce le notifiche supportate dall'interfaccia [**IDot11AdHocManager**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocmanager) . |
| [**IDot11AdHocNetwork**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocnetwork)                                     | Rappresenta una destinazione di rete ad hoc disponibile nell'intervallo di connessione.                            |
| [**IDot11AdHocNetworkNotificationSink**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocnetworknotificationsink)     | Definisce le notifiche supportate dall'interfaccia [**IDot11AdHocNetwork**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocnetwork) . |
| [**IDot11AdHocSecuritySettings**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocsecuritysettings)                   | Specifica le impostazioni di sicurezza per una rete ad hoc wireless.                                         |
| [**IEnumDot11AdHocInterfaces**](/windows/desktop/api/adhoc/nn-adhoc-ienumdot11adhocinterfaces)                       | Rappresenta la raccolta di interfacce di rete ad hoc 802,11 attualmente visibili.                       |
| [**IEnumDot11AdHocNetworks**](/windows/desktop/api/adhoc/nn-adhoc-ienumdot11adhocnetworks)                           | Rappresenta la raccolta di reti ad hoc 802,11 attualmente visibili.                                 |
| [**IEnumDot11AdHocSecuritySettings**](/windows/desktop/api/adhoc/nn-adhoc-ienumdot11adhocsecuritysettings)           | Rappresenta la raccolta di impostazioni di sicurezza associate a ogni rete wireless ad hoc visibile.   |



 

> [!Note]  
> La modalità ad hoc potrebbe non essere disponibile nelle versioni future di Windows. A partire da Windows 8.1 e Windows Server 2012 R2, usare invece [Wi-Fi Direct](about-the-wi-fi-direct-api.md) .

 

 

 



