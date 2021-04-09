---
title: Tipi firmati e non firmati (RPC)
description: I compilatori che utilizzano valori predefiniti diversi per i tipi firmati e non firmati possono causare errori software nell'applicazione distribuita.
ms.assetid: 0464d465-84b7-49fc-968e-5efe037966c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 453d45d0a4c29a2e30449fb645e6f40338eac546
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "103873225"
---
# <a name="signed-and-unsigned-types-rpc"></a>Tipi firmati e non firmati (RPC)

I compilatori che utilizzano valori predefiniti diversi per i tipi firmati e non firmati possono causare errori software nell'applicazione distribuita. È possibile evitare questi problemi dichiarando in modo esplicito i tipi di **carattere come con segno o** **senza segno**.

MIDL definisce il tipo [**piccolo**](/windows/desktop/Midl/small) per assumere lo stesso segno predefinito del tipo **char** nel compilatore C di destinazione. Se il compilatore presuppone che **char** sia senza segno, anche **small** verrà definito come senza segno. Molti compilatori C consentono di modificare l'impostazione predefinita come opzione della riga di comando. Ad esempio, l'opzione della riga di comando **/J** del compilatore C Microsoft modifica il segno predefinito di **char** da signed a unsigned.

È anche possibile controllare il segno di variabili di tipo **char** e **small** con l'opzione della riga di comando del compilatore MIDL [**/char**](/windows/desktop/Midl/-char). Questa opzione consente di specificare il segno predefinito usato dal compilatore. Il compilatore MIDL dichiara in modo esplicito il segno di tutti i tipi **char** che non corrispondono al tipo predefinito del compilatore C nel file di intestazione generato.

 

 
