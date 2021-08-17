---
title: Intestazione ACF
description: L'intestazione ACF contiene attributi specifici della piattaforma che si applicano all'intera interfaccia. Gli attributi applicati a singoli tipi e funzioni nel corpo di ACF eseguono l'override degli attributi nell'intestazione ACF. Non sono necessari attributi nell'intestazione ACF.
ms.assetid: c09ec0f2-2302-450a-b74b-c9008beca325
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11bdfeced843337143fd441d816e3b575be2e7ebc7d93000094f8dcd3737a00d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118924611"
---
# <a name="the-acf-header"></a>Intestazione ACF

L'intestazione ACF contiene attributi specifici della piattaforma che si applicano all'intera interfaccia. Gli attributi applicati a singoli tipi e funzioni nel corpo di ACF eseguono l'override degli attributi nell'intestazione ACF. Non sono necessari attributi nell'intestazione ACF.

L'intestazione ACF può includere uno degli attributi seguenti: **\[** [**\_ handle**](/windows/desktop/Midl/auto-handle) **\]** automatico, **\[** [**\_ handle implicito**](/windows/desktop/Midl/implicit-handle) **\]** o handle [**\_ esplicito**](/windows/desktop/Midl/explicit-handle) **\]** . Se **\[ si usa \_ l'handle \]** automatico o **\[ implicito, \_ \]** specifica il tipo di handle di associazione che verrà usato per l'associazione quando una funzione remota non dispone di un parametro dell'handle di associazione esplicito. Quando ACF non è presente o non specifica un handle di associazione automatico, implicito o esplicito, MIDL usa **\[ \_ l'handle \]** automatico per l'associazione implicita.

Il **\[** [**codice**](/windows/desktop/Midl/code) **\]** o **\[** [**nocode**](/windows/desktop/Midl/nocode) **\]** può essere visualizzato nell'intestazione dell'interfaccia, ma quello scelto può essere visualizzato una sola volta. Quando nessuno dei due attributi è presente, il compilatore **\[ usa il codice \]** come impostazione predefinita.

Per altre informazioni, vedere [Attributi ACF.](/windows/desktop/Midl/acf-attributes)

 

 