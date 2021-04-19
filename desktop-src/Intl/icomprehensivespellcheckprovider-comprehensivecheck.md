---
description: 'Controllo ortografico del testo del provider in modo più completo rispetto a ISpellCheckProvider:: check.'
ms.assetid: BD334EB8-4E14-478D-AB2A-E7F863C4BE0F
title: 'Metodo IComprehensiveSpellCheckProvider:: ComprehensiveCheck'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IComprehensiveSpellCheckProvider.ComprehensiveCheck
api_type:
- COM
api_location:
- spellcheckprovider.h
ms.openlocfilehash: d999a90166e0d54d537abc84c30f6c4e0ee3768c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319496"
---
# <a name="icomprehensivespellcheckprovidercomprehensivecheck-method"></a>Metodo IComprehensiveSpellCheckProvider:: ComprehensiveCheck

Controllo ortografico del testo del provider in modo più completo rispetto a [**ISpellCheckProvider:: check**](/windows/desktop/api/Spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-check).

## <a name="syntax"></a>Sintassi


```C++
HRESULT ComprehensiveCheck(
  [in]  PCWSTR             text,
  [out] IEnumSpellingError **result
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*testo* \[ in\]
</dt> <dd>

Testo da controllare.

</dd> <dt>

*risultato* \[ out\]
</dt> <dd>

Risultato del controllo di questo testo, come enumerazione degli errori di ortografia ([**IEnumSpellingError**](/windows/desktop/api/Spellcheck/nn-spellcheck-ienumspellingerror)), se presenti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Valore restituito                                                                             | Descrizione                           |
|------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>\_OK</dt> </dl>         | Successo.<br/>                |
| <dl> <dt>E \_ INVALIDARG</dt> </dl> | il *testo* è una stringa vuota.<br/> |
| <dl> <dt>\_puntatore E</dt> </dl>    | il *testo* è un puntatore null.<br/>  |



 

## <a name="remarks"></a>Commenti

Questa interfaccia non deve essere implementata da un provider di controllo ortografico. Tuttavia, se il provider supporta due "modalità" di controllo ortografico (uno più veloce e più lento ma più completo), deve implementare questa interfaccia nello stesso oggetto che implementa [**ISpellCheckProvider**](/windows/desktop/api/Spellcheckprovider/nn-spellcheckprovider-ispellcheckprovider) per supportare la modalità di controllo più approfondita. Quando un client chiama [**ISpellChecker:: ComprehensiveCheck**](/windows/desktop/api/Spellcheck/nf-spellcheck-ispellchecker-comprehensivecheck), la funzionalità di controllo ortografico [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) il provider per [**IComprehensiveSpellCheckProvider**](/windows/desktop/api/spellcheckprovider/nn-spellcheckprovider-icomprehensivespellcheckprovider)e chiama **IComprehensiveSpellCheckProvider. ComprehensiveCheck** se l'interfaccia è supportata. Se l'interfaccia non è supportata, verrà eseguito automaticamente il fallback a [**ISpellCheckProvider:: check**](/windows/desktop/api/Spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-check).

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IComprehensiveSpellCheckProvider**](/windows/desktop/api/spellcheckprovider/nn-spellcheckprovider-icomprehensivespellcheckprovider)
</dt> <dt>

[**IEnumSpellingError**](/windows/desktop/api/Spellcheck/nn-spellcheck-ienumspellingerror)
</dt> <dt>

[**ISpellChecker:: ComprehensiveCheck**](/windows/desktop/api/Spellcheck/nf-spellcheck-ispellchecker-comprehensivecheck)
</dt> <dt>

[**ISpellCheckProvider**](/windows/desktop/api/Spellcheckprovider/nn-spellcheckprovider-ispellcheckprovider)
</dt> <dt>

[**ISpellCheckProvider:: check**](/windows/desktop/api/Spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-check)
</dt> </dl>

 

 
