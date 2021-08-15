---
description: Viene illustrato come proteggere gli oggetti Account.
ms.assetid: a07ef46e-f4b6-4e21-bdd7-72d03e1c88b3
title: Protezione oggetti account
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c49610827c8f27b2ad1dd645faca1374534b9d4acb8353421fc55901da724dd5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117969760"
---
# <a name="account-object-protection"></a>Protezione oggetti account

[**Gli**](account-object.md) oggetti account sono protetti nel modo seguente:

-   Il gruppo **WORLD** dispone di GENERIC \_ EXECUTE.
-   Il gruppo **LOCAL \_ ADMIN dispone** dell'accesso DACL DELETE, GENERIC \_ \_ READ, GENERIC WRITE, GENERIC \_ EXECUTE e \_ WRITE.
-   Il gruppo **LOCAL \_ ADMIN** viene assegnato come proprietario e come gruppo primario di oggetti Account.

 

 



