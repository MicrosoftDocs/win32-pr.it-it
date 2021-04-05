---
description: Viene descritto il modo in cui l'oggetto criteri è protetto per impostazione predefinita.
ms.assetid: e2d65ebf-5fbd-4e25-9862-a8188abb5492
title: Protezione degli oggetti Criteri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 802fea6ce37a070c8230c3c9993df78a45f439bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750890"
---
# <a name="policy-object-protection"></a>Protezione degli oggetti Criteri

L'oggetto [**criteri**](policy-object.md) è protetto per impostazione predefinita con le impostazioni seguenti:

-   Il mondo locale del gruppo dispone dell' \_ accesso Execute generico.
-   Al sistema ID noto viene concesso \_ l'accesso a tutti i criteri \_ .
-   L'amministratore locale del gruppo locale \_ dispone \_ di accesso generico Read, Generic \_ Write e Generic \_ Execute.
-   L'amministratore locale del gruppo \_ viene assegnato come proprietario e gruppo primario di questo oggetto.

Impossibile creare o eliminare definitivamente l'oggetto [**criteri**](policy-object.md) .

 

 



