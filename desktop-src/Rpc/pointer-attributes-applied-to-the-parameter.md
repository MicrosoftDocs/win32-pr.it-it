---
title: Attributi del puntatore applicati al parametro
description: Ogni attributo del puntatore (\ Ref \, \ Unique \ e \ PTR \) presenta caratteristiche che influiscono sull'allocazione della memoria. Nella tabella seguente sono riepilogate queste caratteristiche.
ms.assetid: 25a609cd-efe7-4cbb-b80e-b6a3ad8cda38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c7710fb3c39702b2b2fdb789ed1218dc88d44ea
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047191"
---
# <a name="pointer-attributes-applied-to-the-parameter"></a>Attributi del puntatore applicati al parametro

Ogni attributo del puntatore ( \[ [ref](/windows/desktop/Midl/ref) \] , \[ [Unique](/windows/desktop/Midl/unique) \] e \[ [ptr](/windows/desktop/Midl/ptr) \] ) presenta caratteristiche che influiscono sull'allocazione di memoria. Nella tabella seguente sono riepilogate queste caratteristiche.



| Puntatore (attributo)       | Client                                                                                                                                                                                                            | Server                                                              |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| Riferimento ( \[ **ref** \] ) | L'applicazione client deve allocare.                                                                                                                                                                                 | Gestione speciale necessaria per i puntatori a **\[ \] livello di nontop**. |
| Univoco ( \[ **univoco** \] ) | Se un parametro, l'applicazione client deve allocare; Se incorporato, può essere null. Se si modifica da null a non null, lo stub client viene allocato; la modifica da un valore diverso da null a null può causare l'isolamento.<br/> |                                                                     |
| Completo ( \[ **ptr** \] )      | Se un parametro, l'applicazione client deve allocare; Se incorporato, può essere null. Se si modifica da null a non null, lo stub client viene allocato; la modifica da un valore diverso da null a null può causare l'isolamento.<br/> |                                                                     |



 

L'attributo **\[ ref \]** indica che il puntatore punta alla memoria valida. Per definizione, l'applicazione client deve allocare tutta la memoria necessaria per i puntatori di riferimento.

Il puntatore univoco può variare da null a non null. Se il puntatore univoco passa da null a non null, viene allocata una nuova memoria nel client. Se il puntatore univoco passa da un valore diverso da null a un valore null, è possibile che venga generato un orfano. Per ulteriori informazioni, vedere [orfano di memoria](memory-orphaning.md).

 

