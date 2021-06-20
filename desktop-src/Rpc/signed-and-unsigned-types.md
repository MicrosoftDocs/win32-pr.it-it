---
title: Tipi con e senza segno (RPC)
description: Informazioni sui tipi firmati e non firmati in RPC. I compilatori che usano tipi predefiniti diversi possono causare errori software nell'applicazione distribuita.
ms.assetid: 0464d465-84b7-49fc-968e-5efe037966c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4c03010262c8492b6738d1e817e165e5ca8f839
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406544"
---
# <a name="signed-and-unsigned-types-rpc"></a>Tipi con e senza segno (RPC)

I compilatori che usano valori predefiniti diversi per i tipi firmati e non firmati possono causare errori software nell'applicazione distribuita. È possibile evitare questi problemi dichiarando in modo esplicito i tipi di carattere **come signed** o **unsigned**.

MIDL definisce il [**tipo piccolo**](/windows/desktop/Midl/small) per assumere lo stesso segno predefinito del tipo **char** nel compilatore C di destinazione. Se il compilatore presuppone che **char** sia senza segno, **anche small** verrà definito come unsigned. Molti compilatori C consentono di modificare il valore predefinito come opzione della riga di comando. Ad esempio, l'opzione della riga di comando **/J** del compilatore Microsoft C modifica il segno predefinito di **char** da signed a unsigned.

È anche possibile controllare il segno delle variabili di tipo **char** e **small** con l'opzione della riga di comando del compilatore MIDL [**/char**](/windows/desktop/Midl/-char). Questa opzione consente di specificare il segno predefinito usato dal compilatore. Il compilatore MIDL dichiara in modo esplicito il segno di tutti i tipi **char** che non corrispondono al tipo predefinito del compilatore C nel file di intestazione generato.

 

 
