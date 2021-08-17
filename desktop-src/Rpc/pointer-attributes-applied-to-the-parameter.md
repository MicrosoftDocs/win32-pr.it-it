---
title: Attributi del puntatore applicati al parametro
description: Ogni attributo del puntatore (\ ref\ , \ unique\ e \ ptr\ ) ha caratteristiche che influiscono sull'allocazione di memoria. La tabella seguente riepiloga queste caratteristiche.
ms.assetid: 25a609cd-efe7-4cbb-b80e-b6a3ad8cda38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bcc6649dc663d7b029a7d7f345719330719d2eb19b6b7a63fa02797c17df16c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118927496"
---
# <a name="pointer-attributes-applied-to-the-parameter"></a>Attributi del puntatore applicati al parametro

Ogni attributo del puntatore ( \[ [ref](/windows/desktop/Midl/ref) \] , \[ [unique](/windows/desktop/Midl/unique) \] e \[ [ptr](/windows/desktop/Midl/ptr)) ha caratteristiche che \] influiscono sull'allocazione della memoria. La tabella seguente riepiloga queste caratteristiche.



| Attributo pointer       | Client                                                                                                                                                                                                            | Server                                                              |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| Riferimento ( \[ **ref** \] ) | L'applicazione client deve allocare.                                                                                                                                                                                 | Gestione speciale necessaria per **\[ i puntatori out \]**-only non di livello superiore. |
| Univoco ( \[ **univoco** \] ) | Se un parametro, l'applicazione client deve allocare; se incorporato, può essere Null. La modifica da null a non Null comporta l'allocazione dello stub del client. La modifica da non Null a Null può causare l'orfano.<br/> |                                                                     |
| Full ( \[ **ptr** \] )      | Se un parametro, l'applicazione client deve allocare; se incorporato, può essere Null. La modifica da null a non Null comporta l'allocazione dello stub del client. La modifica da non Null a Null può causare l'orfano.<br/> |                                                                     |



 

**\[ L'attributo ref \]** indica che il puntatore punta alla memoria valida. Per definizione, l'applicazione client deve allocare tutta la memoria richiesta dai puntatori di riferimento.

Il puntatore univoco può passare da Null a non Null. Se il puntatore univoco cambia da Null a non Null, nel client viene allocata nuova memoria. Se il puntatore univoco cambia da non Null a Null, può verificarsi l'orfano. Per altre informazioni, vedere [Orfana della memoria](memory-orphaning.md).

 

