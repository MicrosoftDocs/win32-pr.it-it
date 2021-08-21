---
title: Tipi con e senza segno (RPC)
description: Informazioni sui tipi con e senza segno in RPC. I compilatori che usano tipi predefiniti diversi possono causare errori software nell'applicazione distribuita.
ms.assetid: 0464d465-84b7-49fc-968e-5efe037966c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e17a2ccf28233bb14e0811e8015c83aede37d60c58fe9411f13806355fdb7f77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120017700"
---
# <a name="signed-and-unsigned-types-rpc"></a>Tipi con e senza segno (RPC)

I compilatori che usano valori predefiniti diversi per i tipi con e senza segno possono causare errori software nell'applicazione distribuita. È possibile evitare questi problemi dichiarando in modo esplicito i tipi di carattere **come con o** senza **segno.**

MIDL definisce il [**tipo small**](/windows/desktop/Midl/small) in modo che accetta lo stesso segno predefinito del **tipo char** nel compilatore C di destinazione. Se il compilatore presuppone che **char** sia senza segno, **anche small** verrà definito come senza segno. Molti compilatori C consentono di modificare il valore predefinito come opzione della riga di comando. Ad esempio, l'opzione della riga di comando **/J** del compilatore Microsoft C modifica il segno predefinito **di char** da signed a unsigned.

È anche possibile controllare il segno delle variabili di tipo **char** e **small** con l'opzione della riga di comando del compilatore MIDL [**/char**](/windows/desktop/Midl/-char). Questa opzione consente di specificare il segno predefinito usato dal compilatore. Il compilatore MIDL dichiara in modo esplicito il segno di tutti i tipi **char** che non corrispondono al tipo predefinito del compilatore C nel file di intestazione generato.

 

 
