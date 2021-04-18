---
description: Un oggetto incorporato è un oggetto di una classe presente in una dichiarazione di classe o istanza di un'altra classe.
ms.assetid: 11a4556b-f682-4850-aedc-793602c5745b
ms.tgt_platform: multiple
title: Incorporamento di oggetti in una classe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39b94296a6869dddca7fd3df08739615a4a0c501
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315996"
---
# <a name="embedding-objects-in-a-class"></a>Incorporamento di oggetti in una classe

Un oggetto incorporato è un oggetto di una classe presente in una dichiarazione di classe o istanza di un'altra classe. La classe [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) , ad esempio, contiene gli oggetti incorporati [**\_ trustee Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) . Ognuno degli oggetti **\_ trustee Win32** contiene un oggetto [**\_ ACE Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) . WMI non limita la profondità a cui una classe può disporre di oggetti incorporati. Tuttavia, l'uso di un'altra progettazione, ad esempio la creazione di una classe di associazione, può creare uno schema più gestibile.

Per ulteriori informazioni sugli oggetti incorporati, vedere gli argomenti seguenti:

-   [Creazione di oggetti incorporati](creating-embedded-objects.md)
-   [Esecuzione di query su oggetti incorporati](querying-embedded-objects.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Progettazione di classi Managed Object Format (MOF)](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 
