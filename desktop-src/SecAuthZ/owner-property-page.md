---
description: L'editor del controllo di accesso può includere una pagina delle proprietà Proprietario che consente all'utente di modificare il proprietario di un oggetto. Per altre informazioni sul proprietario di un oggetto, vedere Proprietario di un nuovo oggetto e Taking Object Ownership in C++.
ms.assetid: b0c421db-450e-4030-98e9-e062202e482c
title: Pagina delle proprietà Proprietario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b67b3707017aa8073cfdf4f5ca64340eda74a640bc604a0bd382b7cf2ebe122e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907661"
---
# <a name="owner-property-page"></a>Pagina delle proprietà Proprietario

L'editor del controllo di accesso può includere una pagina delle proprietà Proprietario che consente all'utente di modificare il proprietario di un oggetto. Per altre informazioni sul proprietario di un oggetto, vedere Proprietario di [un nuovo oggetto](owner-of-a-new-object.md) e Taking Object Ownership in [C++.](taking-object-ownership-in-c--.md)

La **pagina delle** proprietà Proprietario si trova nella [finestra delle](advanced-security-property-sheet.md) proprietà di sicurezza avanzata visualizzata quando l'utente fa clic sul pulsante Avanzate nella pagina [delle proprietà di sicurezza di base](basic-security-property-page.md).  Per includere la pagina delle proprietà **Owner,** impostare i flag SI ADVANCED e SI EDIT OWNER nella struttura SI OBJECT INFO restituita dall'implementazione \_ di \_ \_ [**ISecurityInformation::GetObjectInformation.**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getobjectinformation) [**\_ \_**](/windows/desktop/api/Aclui/ns-aclui-si_object_info)

 

 
