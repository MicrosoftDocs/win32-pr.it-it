---
description: La funzione di esportazione FormatProperties formatta i dati visualizzati nel riquadro dei dettagli dell'Network Monitor interfaccia utente. Per visualizzare i dati nel riquadro dei dettagli, è necessario implementare la funzione di esportazione FormatProperties in tutte le DLL del parser.
ms.assetid: 78e0b4b9-f19e-41cb-8504-635f3f9ac1ee
title: Funzione di callback FormatProperties (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FormatProperties
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 6bb0bc74a52569edbb922aa93edd27b53106073ffdafa3a6cacc5808aab71eef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012249"
---
# <a name="formatproperties-callback-function"></a>Funzione di callback FormatProperties

La funzione di esportazione **FormatProperties** formatta i dati visualizzati nel riquadro dei dettagli dell'Network Monitor interfaccia utente. Per visualizzare i dati nel riquadro dei dettagli, è necessario implementare la funzione di esportazione **FormatProperties** in tutte le DLL del parser.

## <a name="syntax"></a>Sintassi


```C++
DWORD FormatProperties(
  _In_ HFRAME         hFrame,
  _In_ LPBYTE         lpFrame,
  _In_ LPBYTE         lpProtocol,
  _In_ DWORD          nPropertyInsts,
  _In_ LPPROPERTYINST lpPropInst
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hFrame* \[ Pollici\]
</dt> <dd>

Handle per il frame che viene analizzato.

</dd> <dt>

*lpFrame* \[ Pollici\]
</dt> <dd>

Puntatore al primo byte di un frame.

</dd> <dt>

*lpProtocol* \[ Pollici\]
</dt> <dd>

Puntatore all'inizio dei dati del protocollo in un frame.

</dd> <dt>

*nPropertyInsts* \[ Pollici\]
</dt> <dd>

Numero di [strutture PROPERTYINST](propertyinst.md) fornite da *lpPropInst.*

</dd> <dt>

*lpPropInst* \[ Pollici\]
</dt> <dd>

Puntatore a una matrice [di strutture PROPERTYINST.](propertyinst.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è **TRUE.**

Se la funzione ha esito negativo, il valore restituito è **FALSE.**

## <a name="remarks"></a>Commenti

Network Monitor chiama la **funzione FormatProperties** per visualizzare i dati nel riquadro dei dettagli dell'interfaccia Network Monitor interfaccia utente. In genere, **FormatProperties** viene chiamato per formattare la riga di riepilogo per un protocollo e quindi per formattare tutte le istanze di proprietà del protocollo all'interno di un frame. Tuttavia, Network Monitor non garantisce il numero di chiamate a **FormatProperties** per un parser specifico.

Durante l'implementazione della funzione **FormatProperties,** il parser chiama indirettamente la funzione [FormatPropertyInstance](formatpropertyinstance.md) per usare il formattatore generico fornito da Network Monitor oppure può chiamare una routine del formattatore personalizzata definita dal parser. Uno dei formattatori deve essere chiamato per ogni [struttura PROPERTYINST](propertyinst.md) passata alla DLL del parser nel *parametro lpPropInst.*



| Per informazioni su                                          | Vedere                                                                |
|-------------------------------------------------------------|--------------------------------------------------------------------|
| Che cosa sono i parser e come funzionano con Network Monitor.   | [Parser](parsers.md)                                             |
| Punti di ingresso inclusi nella DLL del parser.          | [Architettura della DLL del parser](parser-dll-architecture.md)             |
| Come implementare **FormatProperties**  include un esempio. | [Implementazione di FormatProperties](implementing-formatproperties.md) |
| Modalità di formato dei diversi tipi di dati da parte del formattatore generico.  | [Output del formattatore generico](generic-formatter-output.md)           |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Istanza di FormatProperty](formatpropertyinstance.md)
</dt> <dt>

[Propertyinfo](propertyinfo.md)
</dt> <dt>

[PROPERTYINST](propertyinst.md)
</dt> </dl>

 

 




