---
title: Sviluppo di un provider
description: Per scrivere gli eventi definiti nel manifesto, è possibile usare le funzioni incluse nell'API traccia eventi (ETW). Per informazioni dettagliate sulla scrittura di un provider, vedere la pagina relativa alla fornitura di eventi.
ms.assetid: 23de19c4-5f8d-4faa-acd9-fe6208ca17a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83939429f1dc4d499e7c2d0e0c2bfa7a47522ffe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118315"
---
# <a name="developing-a-provider"></a>Sviluppo di un provider

Per scrivere gli eventi definiti nel manifesto, è possibile usare le funzioni incluse nell'API [traccia eventi](/windows/desktop/ETW/event-tracing-portal) (ETW). Per informazioni dettagliate sulla scrittura di un provider, vedere la pagina relativa alla [fornitura di eventi](/windows/desktop/ETW/providing-events).

Dopo aver scritto il provider, usare lo strumento WevtUtil.exe per registrare il provider e lo schema. Per informazioni dettagliate sull'uso di WevtUtil, vedere [strumenti del registro eventi di Windows](windows-event-log-tools.md). Di seguito viene illustrato come utilizzare WevtUtil per registrare un provider e rimuovere la registrazione.


```cmd
wevtutil im provider.man

wevtutil um provider.man
```