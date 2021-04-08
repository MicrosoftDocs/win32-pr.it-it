---
title: Interfacce duali (ADSI)
description: Utilizzare le interfacce COM per accedere alle proprietà e ai metodi di qualsiasi oggetto ADSI del provider.
ms.assetid: 6f3fd725-d660-4cc3-8de2-8ed7800b1141
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a34c858275098dd82362d229bc9e1cc35b544c55
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730186"
---
# <a name="dual-interfaces-adsi"></a>Interfacce duali (ADSI)

Utilizzare le interfacce COM per accedere alle proprietà e ai metodi di qualsiasi oggetto ADSI del provider. Una proprietà di sola lettura viene mappata a una voce di interfaccia del form **get \_ <PropertyName>**. Una proprietà di lettura/scrittura esegue il mapping a due voci di interfaccia del form **get \_ <PropertyName>** e **put \_ <PropertyName>**.

Tutti i metodi in un'interfaccia COM devono:

-   Restituisce un valore HRESULT per indicare l'esito positivo o negativo. Il tipo **HRESULT** viene descritto nella specifica com.
-   Nelle chiamate a **QueryInterface**, restituire **E \_ nointerface** per le interfacce non implementate.
-   Restituisce **E \_ NOTIMPL** per i metodi non implementati sulle interfacce altrimenti implementate.
-   La **Proprietà return E \_ Ads \_ non è \_ \_ supportata** per le proprietà dell'interfaccia che non sono supportate.

Per mantenere la compatibilità con i controller di automazione, tutti i parametri e i tipi restituiti devono essere inclusi nel subset definito dal tipo di dati VARIANT di automazione. Per ulteriori informazioni, vedere **Variant** e **VARIANTARG** in Platform Software Development Kit (SDK).

Un provider Active Directory oggetto può esporre interfacce che usano tipi di dati diversi da quelli nel subset di **varianti** . Tuttavia, i controller di automazione come Visual Basic non sono in grado di chiamare tali interfacce. La maggior parte delle interfacce del provider ADSI sono derivate da [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) e possono essere usate come puntatori dell'interfaccia **IDispatch** . Tuttavia, le interfacce ADSI [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject), [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)e [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) non sono derivate da **IDispatch**.

 

 