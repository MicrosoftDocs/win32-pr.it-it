---
title: Funzioni Rich Edit
description: Funzioni Rich Edit
ms.assetid: 5e913cb6-d561-447f-b33e-9160a8f46cda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df1b74069b63220a07bfb1bd5e3f5a1ad99a6c6c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482457"
---
# <a name="rich-edit-functions"></a>Funzioni Rich Edit

## <a name="in-this-section"></a>Contenuto della sezione




| Argomento | Descrizione | 
|-------|-------------|
| <a href="/windows/desktop/api/Richedit/nc-richedit-autocorrectproc"><em>AutoCorrectProc</em></a><br /> | La <a href="/windows/desktop/api/Richedit/nc-richedit-autocorrectproc"><em>funzione AutoCorrectProc</em></a> è una funzione di callback definita dall'applicazione usata con il <a href="em-setautocorrectproc.md"><strong>EM_SETAUTOCORRECTPROC</strong></a> messaggio.<br /> | 
| <a href="/windows/desktop/api/Richedit/nc-richedit-editstreamcallback"><em>EditStreamCallback</em></a><br /> | La <a href="/windows/desktop/api/Richedit/nc-richedit-editstreamcallback"><em>funzione EditStreamCallback</em></a> è una funzione di callback definita dall'applicazione usata con i EM_STREAMIN <a href="em-streamin.md"><strong>e</strong></a> <a href="em-streamout.md"><strong>EM_STREAMOUT</strong></a> messaggi. Viene usato per trasferire un flusso di dati all'interno o all'uscita da un controllo Rich Edit. Il <strong>tipo EDITSTREAMCALLBACK</strong> definisce un puntatore a questa funzione di callback. <em>EditStreamCallback è</em> un segnaposto per il nome della funzione definita dall'applicazione. <br /> | 
| <a href="/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex"><em>EditWordBreakProcEx</em></a><br /> | La <a href="/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex"><em>funzione EditWordBreakProcEx</em></a> è una funzione di callback definita dall'applicazione usata con il <a href="em-setwordbreakprocex.md"><strong>EM_SETWORDBREAKPROCEX</strong></a> messaggio. Determina l'indice dei caratteri dell'interruzione di parola o la classe di caratteri e i flag di interruzione di parola dei caratteri nel testo specificato. Il <strong>tipo EDITWORDBREAKPROCEX</strong> definisce un puntatore a questa funzione di callback. <em>EditWordBreakProcEx è</em> un segnaposto per il nome della funzione definita dall'applicazione. <br /> | 
| <a href="/previous-versions/windows/desktop/legacy/hh780353(v=vs.85)"><strong>GetMathAlphanumeric</strong></a><br /> | Recupera il carattere alfanumerico matematico UTF (Unicode Transformation Format)-32 corrispondente al carattere BMP (Basic Multilingual Plane) e allo stile matematico specificati. <br /> | 
| <a href="/previous-versions/windows/desktop/legacy/hh780354(v=vs.85)"><strong>GetMathAlphanumericCode</strong></a><br /> | Recupera lo stile matematico e il codice carattere BMP (Basic Multilingual Plane) verticale corrispondente al byte finale specificato di una coppia di surrogati matematici.<br /> | 
| <a href="/windows/desktop/api/Richedit/nf-richedit-hyphenateproc"><em>HyphenateProc</em></a><br /> | La <a href="/windows/desktop/api/Richedit/nf-richedit-hyphenateproc"><em>funzione HyphenateProc</em></a> è una funzione di callback definita dall'applicazione usata con <a href="em-sethyphenateinfo.md"><strong>EM_SETHYPHENATEINFO</strong></a> messaggio. Determina come viene eseguita la sillabazione in un controllo Microsoft Rich Edit.<br /> | 
| <a href="/previous-versions/windows/desktop/legacy/hh780443(v=vs.85)"><strong>MathBuildDown</strong></a><br /> | Converte in forma lineare gli oggetti matematici, ruby e altri oggetti inline incorporati nell'intervallo specificato.<br /> | 
| <a href="/previous-versions/windows/desktop/legacy/hh780445(v=vs.85)"><strong>MathBuildUp</strong></a><br /> | Converte i calcoli matematici in formato lineare in un intervallo in un formato predefinito o modifica il form predefinito corrente. <br /> | 
| <a href="/previous-versions/windows/desktop/legacy/hh780446(v=vs.85)"><strong>MathTranslate</strong></a><br /> | Converte i caratteri matematici nell'intervallo specificato.<br /> | 
| <a href="reextendedregisterclass.md"><strong>REExtendedRegisterClass</strong></a><br /> | Registra due nomi di classe, REListBox20W e RECombobox20W, che possono essere usati per creare finestre casella di riepilogo o casella combinata Rich Edit. <br /><blockquote>[!Note]<br />Destinato all'uso interno; non consigliato per l'uso nelle applicazioni. Questa funzione potrebbe non essere supportata nelle versioni future.</blockquote><br /> | 




 

 

