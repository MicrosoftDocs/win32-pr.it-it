---
description: Questa sezione descrive le interfacce IMM.
ms.assetid: 25092F1D-0B54-4E5E-AC9E-F8F3A0181482
title: Interfacce di gestione metodi di input
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64bd04c02425aef19ed329867a5b228bd4838af8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312862"
---
# <a name="input-method-manager-interfaces"></a>Interfacce di gestione metodi di input

Questa sezione descrive le interfacce IMM.



| Interfaccia                                                            | Descrizione                                                                                                                                    |
|----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IFECommon**](/windows/desktop/api/Msime/nn-msime-ifecommon)                                       | Fornisce servizi correlati a IME comuni per linguaggi diversi.                                                                         |
| [**IFEDictionary**](/windows/desktop/api/Msime/nn-msime-ifedictionary)                               | Consente ai client di accedere a un dizionario utenti Microsoft IME.                                                                                      |
| [**IFELanguage**](/windows/desktop/api/Msime/nn-msime-ifelanguage)                                   | Fornisce servizi di elaborazione del linguaggio utilizzando Microsoft IME.                                                                                 |
| [**IImePad**](/windows/desktop/api/Imepad/nn-imepad-iimepad)                                           | Inserisce il testo nelle app da IMEPadApplets che implementano l'interfaccia [**IImePadApplet**](/windows/desktop/api/Imepad/nn-imepad-iimepadapplet) .                                 |
| [**IImePadApplet**](/windows/desktop/api/Imepad/nn-imepad-iimepadapplet)                               | Inserisce le stringhe nelle app tramite l'interfaccia [**IImePad**](/windows/desktop/api/Imepad/nn-imepad-iimepad) .                                                                     |
| [**IImePlugInDictDictionaryList**](/windows/desktop/api/Msimeapi/nn-msimeapi-iimeplugindictdictionarylist) | Consente di accedere all'elenco dei dizionari plug-in IME.                                                                                       |
| [**IImeSpecifyApplets**](/windows/desktop/api/Imepad/nn-imepad-iimespecifyapplets)                     | Specifica i metodi chiamati dall'oggetto interfaccia [**IImePad**](/windows/desktop/api/Imepad/nn-imepad-iimepad) per emulare l'interfaccia [**IImePadApplet**](/windows/desktop/api/Imepad/nn-imepad-iimepadapplet) . |



 

 

 



