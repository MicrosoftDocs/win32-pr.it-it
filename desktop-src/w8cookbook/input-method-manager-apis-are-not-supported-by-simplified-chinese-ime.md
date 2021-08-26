---
title: Le API di Gestione metodi di input non sono supportate dall'IME cinese semplificato
description: Le API di Gestione metodi di input non sono supportate dall'IME cinese semplificato
ms.assetid: 829E1920-8A5C-4DBB-A844-72DA75D58B92
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d0454df8df722992e321fd7fc6bd745382ea215116b2fd5a7797f2032a9c7e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119935411"
---
# <a name="input-method-manager-apis-are-not-supported-by-simplified-chinese-ime"></a>Le API di Gestione metodi di input non sono supportate dall'IME cinese semplificato

## <a name="platforms"></a>Piattaforme

<dl> Client - Windows 8.1  
R2 per Windows Server 2012  
</dl>

## <a name="description"></a>Descrizione

Le API di gestione dei metodi di input seguenti non sono supportate dagli IME in cinese semplificato Windows 8.1:

-   Interfaccia IFECommon
-   Interfaccia IFEDictionary
-   Interfaccia IFELanguage
-   Interfaccia IImePad
-   Interfaccia IImePadApplet
-   Interfaccia IImeSpecifyApplets

## <a name="manifestations"></a>Manifestazioni

Le funzioni che usano queste API non funzionano con l'IME cinese semplificato.

## <a name="solution"></a>Soluzione

Le applicazioni devono essere progettate in modo che gli utenti possano completare l'attività desiderata senza usare l'API specificata.

## <a name="resources"></a>Risorse

-   [Interfacce di Gestione metodi di input](../intl/input-method-manager-interfaces.md)
-   [IFECommon](/windows/win32/api/msime/nn-msime-ifecommon)
-   [Interfaccia IFECommon](/windows/win32/api/msime/nn-msime-ifecommon)
-   [Interfaccia IFEDictionary](/windows/win32/api/msime/nn-msime-ifedictionary)
-   [IFELanguage](/windows/win32/api/msime/nn-msime-ifelanguage)
-   [IImePad](/windows/win32/api/imepad/nn-imepad-iimepad)
-   [IImePadApplet](/windows/win32/api/imepad/nn-imepad-iimepadapplet)
-   [IimePlugInDictDictionaryList](/windows/win32/api/msimeapi/nn-msimeapi-iimeplugindictdictionarylist)
-   [IImeSpecifyApplets](/windows/win32/api/imepad/nn-imepad-iimespecifyapplets)

 

 