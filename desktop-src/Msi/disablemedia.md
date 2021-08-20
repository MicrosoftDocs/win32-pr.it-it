---
description: Se questo criterio di sistema per utente è impostato su &\# 0034;1&0034; gli utenti e gli amministratori che eseguono un'installazione di manutenzione di un prodotto non possono usare la finestra di dialogo Sfoglia per esplorare le origini multimediali, ad esempio CD-ROM, per le origini di altri prodotti \# installabili.
ms.assetid: 275a6d43-ecf8-4146-82eb-3b42b25b9a80
title: DisableMedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2337a1698865b0b977e179021f6490e2fa651a8c4baa3a56e808d037926ad39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118143247"
---
# <a name="disablemedia"></a>DisableMedia

Se questo criterio [](system-policy.md) di sistema per utente è impostato su "1", gli utenti e gli amministratori che eseguono un'installazione di manutenzione di un prodotto non possono usare la finestra di dialogo Sfoglia per esplorare le origini dei supporti, ad esempio CD-ROM, per le origini di altri prodotti installabili. La ricerca di altri prodotti non viene consentita indipendentemente dal fatto che l'installazione sia eseguita con privilegi elevati. È comunque possibile che l'utente reinstalli il prodotto dai supporti se l'utente ha un'origine multimediale etichettata correttamente.

## <a name="registry-key"></a>Chiave del Registro di sistema

**HKEY \_ Current \_ USER** \\ **Software** \\ **Policies** \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo di dati

**REG \_ DWORD**

## <a name="remarks"></a>Commenti

Si noti che [**la proprietà DISABLEMEDIA**](-disablemedia.md) ha un effetto diverso rispetto al criterio DisableMedia. L'impostazione dei criteri di sistema DisableMedia disabilita solo l'esplorazione delle origini multimediali. **L'impostazione della proprietà DISABLEMEDIA** impedisce al programma di installazione di registrare qualsiasi origine multimediale, ad esempio un CD-ROM, come origine valida per il prodotto. Se l'esplorazione è abilitata, tuttavia, un utente può comunque passare a un'origine multimediale.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Resilienza dell'origine](source-resiliency.md)
</dt> </dl>

 

 



