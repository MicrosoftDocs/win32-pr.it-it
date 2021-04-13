---
title: Oggetto agente di revoca licenze
description: Oggetto agente di revoca licenze
ms.assetid: 19b0e697-1648-40e3-b6ef-c726905a47a2
keywords:
- Windows Media Format SDK, oggetti dell'agente di revoca delle licenze
- ASF (Advanced Systems Format), oggetti dell'agente di revoca delle licenze
- ASF (formato avanzato dei sistemi), oggetti dell'agente di revoca delle licenze
- oggetti, oggetti dell'agente di revoca delle licenze
- revoca delle licenze, oggetti dell'agente di revoca delle licenze
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11a02e07c0f5e2f25c90b39ffcf21e15048e55dc
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104398548"
---
# <a name="license-revocation-agent-object"></a>Oggetto agente di revoca licenze

L'oggetto agente di revoca licenze gestisce il lato client della revoca delle licenze. La revoca delle licenze è il processo mediante il quale un server licenze può rimuovere le licenze dall'archivio licenze nel computer client. Il processo implica il passaggio di diversi messaggi tra l'applicazione client e il server licenze. I metodi esposti in questo oggetto elaborano e generano tali messaggi.

L'oggetto dell'agente di revoca delle licenze viene creato dalla funzione [**WMCreateLicenseRevocationAgent**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatelicenserevocationagent) , che imposta un puntatore a un'interfaccia [**IWMLicenseRevocationAgent**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserevocationagent) . **IUnknown** e **IWMLicenseRevocationAgent** sono le uniche interfacce supportate da questo oggetto.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Oggetti**](objects.md)
</dt> </dl>

 

 




