---
description: Per impostazione predefinita, tutte le eccezioni FP del sistema sono state disattivate.
ms.assetid: efbea036-de9c-4f92-865a-494161da375e
title: Eccezioni a virgola mobile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6a4db92a13a0215bb372db12d30bb11a749a0fc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304414"
---
# <a name="floating-point-exceptions"></a>Eccezioni a virgola mobile

Per impostazione predefinita, tutte le eccezioni FP del sistema sono state disattivate. Pertanto, i calcoli generano NAN o INFINITY, anziché un'eccezione. Prima di poter intercettare le eccezioni a virgola mobile (FP) utilizzando la gestione delle eccezioni strutturata, è necessario chiamare la funzione della libreria di runtime C di [ \_ controlfp \_ ](/previous-versions/visualstudio/visual-studio-2010/c9676k6h(v=vs.100)) per attivare tutte le eccezioni FP possibili. Per intercettare solo determinate eccezioni, utilizzare solo i flag che corrispondono alle eccezioni da intercettare. Si noti che qualsiasi gestore per gli errori FP deve chiamare [ \_ clearfp](/cpp/c-runtime-library/reference/clear87-clearfp?view=vs-2019) come prima istruzione FP. Questa funzione Cancella le eccezioni a virgola mobile.

 

 
