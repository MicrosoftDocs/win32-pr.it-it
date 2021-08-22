---
description: Se le regole di Selezione predefinita non soddisfano le esigenze dell'applicazione, l'applicazione può selezionare manualmente il terminale.
ms.assetid: 12d7781e-a27d-4cbe-b7c4-6c0dfef11074
title: Selezione manuale del terminale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6eaa1e0a5b8b53b1037c51b0e628d7a27ece0be65a0f9a7e86e882c722360f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119514641"
---
# <a name="manual-terminal-selection"></a>Selezione manuale del terminale

Se le regole di Selezione predefinita non soddisfano le esigenze dell'applicazione, l'applicazione ha la possibilità di selezionare il terminale come sempre: può usare [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) per enumerare i flussi presenti nella chiamata e selezionare il terminale nei flussi appropriati (o, nel caso di terminali multitracking, creare tracce per i flussi e selezionare le tracce create nei flussi).

 

 
