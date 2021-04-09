---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 50397050-3b5c-4683-972c-95d9f661b365
ms.tgt_platform: multiple
title: D (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d469b94ec6649c64722fb414880d2e79fc3c88b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050122"
---
# <a name="d-wmi"></a>D (WMI)

[A](gloss-a.md) B [C](gloss-c.md) d [E](gloss-e.md) [F](gloss-f.md) G [H](gloss-h.md) [i](gloss-i.md) J [K](gloss-k.md) [L](gloss-l.md) [M](gloss-m.md) [N](gloss-n.md) [O](gloss-o.md) [P](gloss-p.md) [Q](gloss-q.md) [R](gloss-r.md) [S](gloss-s.md) [T](gloss-t.md) U V [W](gloss-w.md) X Y Z

<dl> <dt>

<span id="wmi.gloss_datetime"></span><span id="WMI.GLOSS_DATETIME"></span>**DateTime**
</dt> <dd>

Vedere [*CIM DateTime*](gloss-c.md).

</dd> <dt>

<span id="wmi.gloss_decoupled_provider"></span><span id="WMI.GLOSS_DECOUPLED_PROVIDER"></span>**provider disaccoppiato**
</dt> <dd>

Provider gestito in un processo distinto da WMI. I provider disaccoppiati sono il metodo consigliato per instrumentare un'applicazione, poiché il provider può controllare la propria durata anziché essere avviato ogni volta che un utente accede al provider tramite WMI.

</dd> <dt>

<span id="wmi.gloss_direct_access"></span><span id="WMI.GLOSS_DIRECT_ACCESS"></span>**accesso diretto**
</dt> <dd>

Un modo per accedere alle proprietà e ai metodi forniti da WMI in uno script come se si trattasse di proprietà e metodi di automazione di [**SWbemObject**](swbemobject.md).

Accesso non diretto: `VolumeName = MyDisk.Properties_("VolumeName")`

Accesso diretto: `VolumeName = MyDisk.VolumeName`

</dd> <dt>

<span id="wmi.gloss_distributed_management_task_force"></span><span id="WMI.GLOSS_DISTRIBUTED_MANAGEMENT_TASK_FORCE"></span>**Distributed Management Task Force (DMTF)**
</dt> <dd>

Un'organizzazione di standard internazionali che interagisce con i fornitori di tecnologie principali, tra cui Microsoft, per condurre lo sviluppo, l'adozione e l'unificazione degli standard di gestione e delle iniziative per ambienti desktop, aziendali e Internet.

</dd> <dt>

<span id="wmi.gloss_dmtf"></span><span id="WMI.GLOSS_DMTF"></span>**DMTF**
</dt> <dd>

Vedere *Distributed Management Task Force (DMTF)*.

</dd> <dt>

<span id="wmi.gloss_dynamic_class"></span><span id="WMI.GLOSS_DYNAMIC_CLASS"></span>**classe dinamica**
</dt> <dd>

Classe CIM la cui definizione viene fornita da un [*provider*](gloss-p.md) in fase di esecuzione, in base alle esigenze. Le classi dinamiche rappresentano [*oggetti gestiti*](gloss-m.md) specifici del provider e non vengono archiviati nel [*repository CIM*](gloss-c.md). Le classi dinamiche supportano solo le *istanze dinamiche*.

</dd> <dt>

<span id="wmi.gloss_dynamic_instance"></span><span id="WMI.GLOSS_DYNAMIC_INSTANCE"></span>**istanza dinamica**
</dt> <dd>

Istanza di una classe CIM fornita da un [*provider*](gloss-p.md) quando richiesto. Non è archiviato nel [*repository CIM*](gloss-c.md). Le istanze dinamiche possono essere fornite per classi statiche o dinamiche. Il supporto dinamico di istanze di una classe consente a un provider di fornire i valori delle [*Proprietà*](gloss-p.md) fino al minuto.

</dd> </dl>

 

 



