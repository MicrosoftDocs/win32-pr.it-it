---
description: La configurazione dei criteri IPSec e delle associazioni di sicurezza per IPv6 viene eseguita con Ipsec6.exe.
ms.assetid: 9a0c8e48-bc57-461d-9ade-54b75f7aa56d
title: Ipsec6.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b373e8ab0dc54c3c8ee2fae8bc05722a9ac6aa64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306945"
---
# <a name="ipsec6exe"></a>Ipsec6.exe

La configurazione dei criteri IPSec e delle associazioni di sicurezza per IPv6 viene eseguita con Ipsec6.exe. Di seguito sono Ipsec6.exe sottocomandi:

<dl> <dt>

<span id="ipsec6_sp__Interface_"></span><span id="ipsec6_sp__interface_"></span><span id="IPSEC6_SP__INTERFACE_"></span>**SP \[ ipsec6** _Interfaccia_ di *_\]_*
</dt> <dd>

Visualizza i criteri di sicurezza attivi. In alternativa, Visualizza i criteri di sicurezza attivi per un'interfaccia specifica.

</dd> <dt>

<span id="ipsec6_sa"></span><span id="IPSEC6_SA"></span>**sa ipsec6**
</dt> <dd>

Visualizza le associazioni di sicurezza attive.

</dd> <dt>

<span id="ipsec6_c__FileName_without_extension__"></span><span id="ipsec6_c__filename_without_extension__"></span><span id="IPSEC6_C__FILENAME_WITHOUT_EXTENSION__"></span>**ipsec6 c \[** _FileName (senza estensione)_*_\]_*
</dt> <dd>

Crea i file utilizzati per configurare i criteri di sicurezza e le associazioni di sicurezza. Crea *filename*. SPD per i criteri di sicurezza e *filename*. Sad per le associazioni di sicurezza. Usare i file creati come modelli per configurare i criteri di sicurezza o le associazioni di sicurezza. I file possono essere modificati con un editor di testo. Per richiamare la configurazione contenuta nei file SPD e SAD, utilizzare il comando **ipsec6 a** .

</dd> <dt>

<span id="ipsec6_a__FileName_without_extension__"></span><span id="ipsec6_a__filename_without_extension__"></span><span id="IPSEC6_A__FILENAME_WITHOUT_EXTENSION__"></span>**ipsec6 \[** _FileName (senza estensione)_*_\]_*
</dt> <dd>

Aggiunge i criteri di sicurezza in *filename*. SPD e le associazioni di sicurezza in *filename*. Sad all'elenco dei criteri di sicurezza e delle associazioni di sicurezza attivi.

</dd> <dt>

<span id="ipsec6_i__Policy___FileName_without_extension__"></span><span id="ipsec6_i__policy___filename_without_extension__"></span><span id="IPSEC6_I__POLICY___FILENAME_WITHOUT_EXTENSION__"></span>**ipsec6 \[**  *_\] \[_* _Nome file criterio (senza estensione)_*_\]_*
</dt> <dd>

Aggiunge i criteri di sicurezza in *filename*. SPD e le associazioni di sicurezza in *filename*. Sad all'elenco dei criteri di sicurezza attivi e delle associazioni di sicurezza, come a cui fa riferimento il numero di criteri.

</dd> <dt>

<span id="ipsec6_d__type___sp_sa___IndexNumber_"></span><span id="ipsec6_d__type___sp_sa___indexnumber_"></span><span id="IPSEC6_D__TYPE___SP_SA___INDEXNUMBER_"></span>**ipsec6 d \[ Type = SP sa \] \[** _NumeroIndice_*_\]_*
</dt> <dd>

Elimina i criteri di sicurezza o le associazioni di sicurezza dall'elenco dei criteri di sicurezza attivi e delle associazioni di sicurezza, come a cui fa riferimento il numero di indice (visualizzato con **ipsec6 sp** o **ipsec6 sa**).

</dd> </dl>

 

 



