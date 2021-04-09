---
description: Se il criterio di sistema per utente è impostato su &\# 0034; 1&\# 0034;, gli utenti e gli amministratori che eseguono un'installazione di manutenzione di un prodotto non possono utilizzare la finestra di dialogo Sfoglia per visualizzare le origini multimediali, ad esempio CD-ROM, per le origini di altri prodotti installabili.
ms.assetid: 275a6d43-ecf8-4146-82eb-3b42b25b9a80
title: DisableMedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2ee50abf36225aa96e52332a53f0b2ab36f058c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "103968844"
---
# <a name="disablemedia"></a>DisableMedia

Se il [criterio di sistema](system-policy.md) per utente è impostato su "1", per gli utenti e gli amministratori che eseguono un'installazione di manutenzione di un prodotto non è possibile utilizzare la finestra di dialogo Sfoglia per visualizzare le origini dei file multimediali, ad esempio CD-ROM, per le origini di altri prodotti installabili. L'esplorazione di altri prodotti viene impedita indipendentemente dal fatto che l'installazione venga eseguita con privilegi elevati. È comunque possibile che l'utente reinstalli il prodotto da un supporto se l'utente dispone di un'origine multimediale correttamente etichettata.

## <a name="registry-key"></a>Chiave del Registro di sistema

**HKEY \_ Criteri \_ software utente correnti** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo di dati

**REG \_ DWORD**

## <a name="remarks"></a>Commenti

Si noti che la proprietà [**DISABLEMEDIA**](-disablemedia.md) ha un effetto diverso rispetto al criterio DISABLEMEDIA. Se si imposta il criterio di sistema DisableMedia, viene disabilitato solo l'esplorazione delle origini multimediali. L'impostazione della proprietà **DISABLEMEDIA** impedisce al programma di installazione di registrare qualsiasi origine multimediale, ad esempio un CD-ROM, come origine valida per il prodotto. Se l'esplorazione è abilitata, tuttavia, un utente può comunque passare a un'origine multimediale.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Resilienza di origine](source-resiliency.md)
</dt> </dl>

 

 



