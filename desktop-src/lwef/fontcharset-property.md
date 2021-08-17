---
title: Proprietà FontCharSet
description: Proprietà FontCharSet
ms.assetid: 2f23a242-d620-4766-8f59-cf158aa55969
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca702bb1ff9dfe020f7fdb43b57a74fd1e5e46a14caff8735f21170ed8e2f1b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118479329"
---
# <a name="fontcharset-property"></a>Proprietà FontCharSet

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce o imposta il set di caratteri per il tipo di carattere visualizzato nel fumetto del carattere specificato.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agent***. Caratteri ("**_CharacterID_*_"). Valore Balloon.FontCharSet_ *  \[  =  \]



| Parte    | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *value* | Valore intero che specifica il set di caratteri utilizzato dal tipo di carattere. Di seguito sono riportate alcune impostazioni comuni per il valore: 0 Caratteri Windows standard (ANSI).<br/> 1 Set di caratteri predefinito.<br/> 2 Set di caratteri dei simboli.<br/> 128 Set di caratteri a byte doppio (DBCS) univoco per la versione giapponese di Windows.<br/> 129 Set di caratteri a byte doppio (DBCS) univoco per la versione coreana di Windows.<br/> 134 Set di caratteri a byte doppio (DBCS) univoco per la versione cinese semplificata di Windows.<br/> 136 Set di caratteri a byte doppio (DBCS) univoco per la versione cinese tradizionale di Windows.<br/> 255 Caratteri estesi normalmente visualizzati dalle applicazioni Microsoft MS-DOS.<br/> Per altri valori del set di caratteri, vedere la documentazione di Platform SDK.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Il valore predefinito per il set di caratteri del fumetto di un carattere è impostato nell'editor di caratteri di Microsoft Agent. Inoltre, l'utente può eseguire l'override delle impostazioni del set di caratteri per tutti i caratteri nella finestra delle proprietà di Microsoft Agent.

Questa proprietà si applica solo all'uso del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.

> [!Note]  
> Se si usa un carattere che non è stato compilato, controllare le proprietà [**FontName**](fontname-property.md) e **FontCharSet** per il carattere per determinare se sono appropriate per le impostazioni locali. Potrebbe essere necessario impostare questi valori prima di usare il [**metodo Speak**](speak-method.md) per garantire la visualizzazione del testo appropriato all'interno del fumetto della parola.

 

## <a name="see-also"></a>Vedere anche

[**Proprietà FontName**](fontname-property.md)


 

 





