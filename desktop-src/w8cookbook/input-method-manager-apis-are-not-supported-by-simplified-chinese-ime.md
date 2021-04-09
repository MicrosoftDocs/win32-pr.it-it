---
title: Le API di input Method Manager non sono supportate dall'IME cinese semplificato
description: Le API di input Method Manager non sono supportate dall'IME cinese semplificato
ms.assetid: 829E1920-8A5C-4DBB-A844-72DA75D58B92
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d01d79d569ee7c72508bc217b68bcdf784f0d61
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118011"
---
# <a name="input-method-manager-apis-are-not-supported-by-simplified-chinese-ime"></a>Le API di input Method Manager non sono supportate dall'IME cinese semplificato

## <a name="platforms"></a>Piattaforme

<dl> Client-Windows 8.1  
Windows Server 2012 R2  
</dl>

## <a name="description"></a>Descrizione

Le seguenti API del gestore del metodo di input non sono supportate dagli IME cinese semplificato in Windows 8.1:

-   Interfaccia IFECommon
-   Interfaccia IFEDictionary
-   Interfaccia IFELanguage
-   Interfaccia IImePad
-   Interfaccia IImePadApplet
-   Interfaccia IImeSpecifyApplets

## <a name="manifestations"></a>Manifestazioni

Le funzioni che usano tali API non funzionano con l'IME cinese semplificato.

## <a name="solution"></a>Soluzione

Le applicazioni devono essere progettate in modo che gli utenti possano completare l'attività desiderata senza usare l'API specificata.

## <a name="resources"></a>Risorse

-   [Interfacce di gestione metodi di input](../intl/input-method-manager-interfaces.md)
-   [IFECommon](/windows/win32/api/msime/nn-msime-ifecommon)
-   [Interfaccia IFECommon](/windows/win32/api/msime/nn-msime-ifecommon)
-   [Interfaccia IFEDictionary](/windows/win32/api/msime/nn-msime-ifedictionary)
-   [IFELanguage](/windows/win32/api/msime/nn-msime-ifelanguage)
-   [IImePad](/windows/win32/api/imepad/nn-imepad-iimepad)
-   [IImePadApplet](/windows/win32/api/imepad/nn-imepad-iimepadapplet)
-   [IimePlugInDictDictionaryList](/windows/win32/api/msimeapi/nn-msimeapi-iimeplugindictdictionarylist)
-   [IImeSpecifyApplets](/windows/win32/api/imepad/nn-imepad-iimespecifyapplets)

 

 