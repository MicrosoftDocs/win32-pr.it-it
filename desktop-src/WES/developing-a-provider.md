---
title: Sviluppo di un provider
description: Per scrivere gli eventi definiti nel manifesto, usare le funzioni incluse nell'API Event Tracing (ETW). Per informazioni dettagliate sulla scrittura di un provider, vedere Fornire eventi.
ms.assetid: 23de19c4-5f8d-4faa-acd9-fe6208ca17a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bdcbf17113eb926aba245f270b84e7ab50bf3072e15a9a7752b8828296a00a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117937186"
---
# <a name="developing-a-provider"></a>Sviluppo di un provider

Per scrivere gli eventi definiti nel manifesto, usare le funzioni incluse nell'API [Event Tracing](/windows/desktop/ETW/event-tracing-portal) (ETW). Per informazioni dettagliate sulla scrittura di un provider, vedere [Fornire eventi](/windows/desktop/ETW/providing-events).

Dopo aver scritto il provider, usare lo WevtUtil.exe per registrare il provider e lo schema. Per informazioni dettagliate sull'uso di WevtUtil, vedere Windows [Event Log Tools](windows-event-log-tools.md). Di seguito viene illustrato come usare WevtUtil per registrare un provider e rimuovere la registrazione.


```cmd
wevtutil im provider.man

wevtutil um provider.man
```