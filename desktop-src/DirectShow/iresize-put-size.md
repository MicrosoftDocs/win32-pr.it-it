---
description: Il \_ metodo Put size imposta le dimensioni di output e la modalità di estensione.
ms.assetid: 1186eee4-b5c1-4216-abb3-86ea03b2da40
title: 'IResize: metodo:p ut_Size (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize.put_Size
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 579cee086798e64abd07b25cc4f7bb14405157dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326991"
---
# <a name="iresizeput_size-method"></a>IResize: metodo di \_ dimensioni ut:p

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `put_Size` metodo imposta le dimensioni di output e la modalità di estensione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_Size(
  [in] int Height,
  [in] int Width,
  [in] int Flags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Altezza* \[ in\]
</dt> <dd>

Altezza del video in pixel.

</dd> <dt>

*Larghezza* \[ in\]
</dt> <dd>

Larghezza del video in pixel.

</dd> <dt>

*Flag* \[ in\]
</dt> <dd>

Modalità di estensione. Per i valori possibili, vedere [**ridimensionare i flag**](resize-flags.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** .

## <a name="remarks"></a>Commenti

DES può chiamare questo metodo prima o dopo la chiamata di **put \_ mediaType**. Se DES chiama questo metodo prima di chiamare **put \_ mediaType**, il filtro deve selezionare un valore predefinito per la profondità del bit e usare i valori delle dimensioni per costruire un tipo di supporto di output. Se DES chiama questo metodo dopo avere chiamato **put \_ mediaType**, il filtro deve modificare il tipo di output corrente con le nuove dimensioni.

DES può anche chiamare questo metodo dopo la connessione del PIN di output. In tal caso, modificare il tipo di output e riconnettere il pin di output con il nuovo tipo. Per ulteriori informazioni, vedere [riconnessione dei pin](reconnecting-pins.md) .

Il parametro *Flags* specifica il modo in cui il filtro deve eseguire l'operazione di ridimensionamento.

> [!Note]  
> Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Versione<br/> | DirectX 9,0 o versione successiva<br/>                                                         |
| Intestazione<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> <dt>

[**Interfaccia IResize**](iresize.md)
</dt> </dl>

 

 




