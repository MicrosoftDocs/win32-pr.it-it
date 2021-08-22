---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: d426673b-dea2-4f8b-9259-6a17543f70c0
ms.tgt_platform: multiple
title: P (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 230d3dba8be620b0d2d473dbf23960fff79cb7c76abc8a686c47a630605318d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050789"
---
# <a name="p-wmi"></a>P (WMI)

[A](gloss-a.md) B [C](gloss-c.md) [D](gloss-d.md) [E](gloss-e.md) [F](gloss-f.md) G [H](gloss-h.md) [I](gloss-i.md) J [K](gloss-k.md) [L](gloss-l.md) [M](gloss-m.md) [N](gloss-n.md) [O](gloss-o.md) P [Q](gloss-q.md) R [S](gloss-r.md) [](gloss-s.md) [T U](gloss-t.md) V [W](gloss-w.md) X Y Z

<dl> <dt>

<span id="wmi.gloss_performance_counter"></span><span id="WMI.GLOSS_PERFORMANCE_COUNTER"></span>**contatore delle prestazioni**
</dt> <dd>

Proprietà in una classe di prestazioni derivata da [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) che archivia i dati sulle prestazioni.

</dd> <dt>

<span id="wmi.gloss_performance_object"></span><span id="WMI.GLOSS_PERFORMANCE_OBJECT"></span>**oggetto prestazioni**
</dt> <dd>

Oggetto in una libreria delle prestazioni che archivia i dati nei contatori. Questi oggetti sono visibili nell'utilità [*Monitoraggio di*](gloss-s.md) sistema. Ad esempio, gli oggetti Cache e Logical Disk. Quando viene trasferito in WMI dal [*processo ADAP,*](gloss-a.md) ogni oggetto diventa due classi di prestazioni WMI. Una classe, contenente dati non elaborati, deriva da [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata). L'altra classe deriva da [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) e contiene gli stessi dati visibili in Monitoraggio di sistema calcolati dal provider di contatori cotti.

</dd> <dt>

<span id="wmi.gloss_permanent_consumer"></span><span id="WMI.GLOSS_PERMANENT_CONSUMER"></span>**consumer permanente**
</dt> <dd>

Consumer [*di eventi la*](gloss-e.md) cui registrazione dura fino a quando non viene annullata in modo esplicito. Vedere anche [*consumer temporaneo.*](gloss-t.md)

</dd> <dt>

<span id="wmi.gloss_physical_consumer"></span><span id="WMI.GLOSS_PHYSICAL_CONSUMER"></span>**consumer fisico**
</dt> <dd>

Oggetto COM implementato da un [*provider di consumer*](gloss-e.md) di eventi che include un [*sink*](gloss-s.md) per la ricezione di notifiche degli eventi.

</dd> <dt>

<span id="wmi.gloss_property"></span><span id="WMI.GLOSS_PROPERTY"></span>**Proprietà**
</dt> <dd>

Coppia nome/valore che descrive un'unità di dati per una classe. I valori delle proprietà devono avere un [*tipo di Managed Object Format (MOF)*](gloss-m.md) valido. Vedere anche [*la proprietà di riferimento*](gloss-r.md).

</dd> <dt>

<span id="wmi.gloss_property_provider"></span><span id="WMI.GLOSS_PROPERTY_PROVIDER"></span>**provider di proprietà**
</dt> <dd>

Un server COM che supporta il recupero e la modifica delle proprietà WMI. I provider di proprietà implementano [**le interfacce IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) e [**IWbemPropertyProvider.**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider)

</dd> <dt>

<span id="wmi.gloss_provider"></span><span id="WMI.GLOSS_PROVIDER"></span>**Provider**
</dt> <dd>

Un server COM che comunica con oggetti gestiti per accedere ai dati e alle notifiche degli eventi, ad esempio il Registro di sistema o un dispositivo SNMP. I provider inoltrano questi dati [*al*](gloss-c.md) CIM Object Manager per l'integrazione e l'interpretazione.

</dd> <dt>

<span id="wmi.gloss_provider_method"></span><span id="WMI.GLOSS_PROVIDER_METHOD"></span>**metodo provider**
</dt> <dd>

Metodo implementato da un *provider* WMI.

</dd> </dl>

 

 
