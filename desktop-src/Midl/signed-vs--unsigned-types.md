---
title: Tipi con e senza segno (MIDL)
description: Informazioni sui tipi con e senza segno in MIDL. I compilatori che usano tipi predefiniti diversi possono causare errori software nell'applicazione distribuita.
ms.assetid: a4c2d811-6cf4-4c0b-af12-bf8247152984
keywords:
- tipi di dati MIDL, con segno e senza segno
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2a3ed3c9f7022123f162fe0240ae190cdb4c8f8
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407384"
---
# <a name="signed-and-unsigned-types-midl"></a>Tipi con e senza segno (MIDL)

I compilatori che usano valori predefiniti diversi per i tipi con e senza segno possono causare errori software nell'applicazione distribuita. È possibile evitare questi problemi dichiarando in modo esplicito i tipi di carattere come con o senza segno. Si noti che i compilatori IDL DCE non riconoscono la parola chiave [**firmata**](signed.md). Pertanto, questa funzionalità non è disponibile quando si usa l'opzione del compilatore **MIDL/osf.**

MIDL definisce il [**tipo small**](small.md) in modo che accetta lo stesso segno predefinito del [**tipo char**](char-idl.md) nel compilatore C di destinazione. Se il compilatore presuppone che **char** sia senza segno, **anche small** verrà definito come senza segno. Molti compilatori C consentono di modificare il valore predefinito come opzione della riga di comando. Nell'ambiente di sviluppo Microsoft Visual C++, ad esempio, l'opzione della riga di comando **/J** modifica il segno predefinito di **char** da signed a unsigned.

È anche possibile controllare il segno delle variabili di tipo [**char**](char-idl.md) e [**small**](small.md) con l'opzione della riga di comando del compilatore MIDL [**/char**](-char.md). Questa opzione consente di specificare il segno predefinito usato dal compilatore. Il compilatore MIDL dichiara in modo esplicito il segno di tutti i tipi **char** che non corrispondono al tipo predefinito del compilatore C nel file di intestazione generato.

 

 




