---
description: Descrive come l'oggetto Policy è protetto per impostazione predefinita.
ms.assetid: e2d65ebf-5fbd-4e25-9862-a8188abb5492
title: Protezione degli oggetti criteri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3317d9cef2a6ff1dfa29753f9a807286d62f31abb0e8c0c9d0150ee10535a1fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118894061"
---
# <a name="policy-object-protection"></a>Protezione degli oggetti criteri

[**L'oggetto**](policy-object.md) Policy è protetto per impostazione predefinita con le impostazioni seguenti:

-   Il gruppo locale WORLD dispone \_ dell'accesso GENERIC EXECUTE.
-   Al sistema di ID noto viene concesso l'accesso POLICY \_ \_ ALL.
-   Il gruppo locale LOCAL \_ ADMIN dispone dell'accesso GENERIC \_ READ, GENERIC WRITE e GENERIC \_ \_ EXECUTE.
-   Il gruppo LOCAL \_ ADMIN viene assegnato come proprietario e come gruppo primario di questo oggetto.

[**L'oggetto Policy**](policy-object.md) non può essere creato o eliminato.

 

 



