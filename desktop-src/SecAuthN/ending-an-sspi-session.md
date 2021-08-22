---
description: Quando il client ha terminato la comunicazione con qualsiasi server o ha terminato di usare le credenziali aggiuntive passate alla funzione AcquireCredentialsHandle, il client deve chiamare la funzione FreeCredentialsHandle.
ms.assetid: fa943e9b-d379-441f-8c6e-f0a0f5f7f1a3
title: Chiusura di una sessione SSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4669d3143b480df20f1a5f1d76e73cc75802766d1db83da9b75d304e256ae4dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008269"
---
# <a name="ending-an-sspi-session"></a>Chiusura di una sessione SSPI

Al termine della comunicazione tra client e server, entrambi i lati chiamano la [**funzione DeleteSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-deletesecuritycontext) con i rispettivi handle di contesto. Quando il client ha terminato la comunicazione con qualsiasi server o ha terminato di usare le credenziali aggiuntive passate alla funzione [**AcquireCredentialsHandle,**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) il client deve chiamare la [**funzione FreeCredentialsHandle.**](/windows/desktop/api/Sspi/nf-sspi-freecredentialshandle) Quando il server è pronto per l'arresto e prima di scaricare la DLL, il server deve chiamare **DeleteSecurityContext**.

 

 
