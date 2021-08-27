---
title: Interfacce duali (ADSI)
description: Usare le interfacce COM per accedere alle proprietà e ai metodi in qualsiasi oggetto ADSI del provider.
ms.assetid: 6f3fd725-d660-4cc3-8de2-8ed7800b1141
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60d1cf89ef07e573be8f59805034ff8c567e75fd
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884052"
---
# <a name="dual-interfaces-adsi"></a>Interfacce duali (ADSI)

Usare le interfacce COM per accedere alle proprietà e ai metodi in qualsiasi oggetto ADSI del provider. Una proprietà di sola lettura esegue il mapping a una voce di interfaccia nel formato **get \_ &lt; PropertyName &gt;**. Una proprietà di lettura/scrittura esegue il mapping a due voci di interfaccia nel formato **get \_ &lt; PropertyName &gt;** e **put \_ &lt; PropertyName &gt;**.

Tutti i metodi in un'interfaccia COM devono:

-   Restituisce un valore HRESULT per indicare l'esito positivo o negativo. Il **tipo HRESULT** viene illustrato nella specifica COM.
-   Nelle chiamate a **QueryInterface,** restituisce **E \_ NOINTERFACE** per le interfacce non implementate.
-   Restituisce **E \_ NOTIMPL** per metodi non implementati su interfacce altrimenti implementate.
-   Restituisce **E \_ ADS PROPERTY NOT SUPPORTED \_ \_ \_ per** le proprietà di interfaccia non supportate.

Per mantenere la compatibilità con i controller di Automazione, tutti i parametri e i tipi restituiti devono essere all'interno del subset definito dal tipo di dati VARIANT di Automazione. Per altre informazioni, vedere **VARIANT** e **VARIANTARG** in Platform Software Development Kit (SDK).

Un oggetto Active Directory del provider può esporre interfacce che usano tipi di dati diversi da quelli del subset **VARIANT.** Tuttavia, i controller di automazione Visual Basic non sono in grado di chiamare tali interfacce. La maggior parte delle interfacce del provider ADSI deriva da [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) e può essere usata come **puntatori all'interfaccia IDispatch.** Tuttavia, le interfacce ADSI [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject), [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)e [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) non derivano da **IDispatch**.

 

 
