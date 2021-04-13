---
title: Tipi signed e unsigned (MIDL)
description: I compilatori che utilizzano valori predefiniti diversi per i tipi firmati e non firmati possono causare errori software nell'applicazione distribuita.
ms.assetid: a4c2d811-6cf4-4c0b-af12-bf8247152984
keywords:
- tipi di dati MIDL, signed e unsigned
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e38fbe1dc27eebae7c7933db1d699600370d960
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104400070"
---
# <a name="signed-and-unsigned-types-midl"></a>Tipi signed e unsigned (MIDL)

I compilatori che utilizzano valori predefiniti diversi per i tipi firmati e non firmati possono causare errori software nell'applicazione distribuita. È possibile evitare questi problemi dichiarando in modo esplicito i tipi di carattere come con segno o senza segno. Si noti che i compilatori IDL DCE non riconoscono la parola chiave [**signed**](signed.md). Questa funzionalità non è pertanto disponibile quando si usa l'opzione del compilatore MIDL/**OSF** .

MIDL definisce il tipo [**piccolo**](small.md) per assumere lo stesso segno predefinito del tipo [**char**](char-idl.md) nel compilatore C di destinazione. Se il compilatore presuppone che **char** sia senza segno, anche **small** verrà definito come senza segno. Molti compilatori C consentono di modificare l'impostazione predefinita come opzione della riga di comando. Nell'ambiente di sviluppo Microsoft Visual C++, ad esempio, l'opzione della riga di comando **/J** modifica il segno predefinito di **char** da signed a unsigned.

È anche possibile controllare il segno di variabili di tipo [**char**](char-idl.md) e [**small**](small.md) con l'opzione della riga di comando del compilatore MIDL [**/char**](-char.md). Questa opzione consente di specificare il segno predefinito usato dal compilatore. Il compilatore MIDL dichiara in modo esplicito il segno di tutti i tipi **char** che non corrispondono al tipo predefinito del compilatore C nel file di intestazione generato.

 

 




